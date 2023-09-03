
<script lang='ts'>
	import { appWindow } from '@tauri-apps/api/window'
	import { getWindowHandler } from '$scripts/app/window'
	import { onDestroy, onMount } from 'svelte'
	import IconButton from './generic/buttons/IconButton.svelte'
	import { windowTitle } from '$stores/app'

	// get controls for the main window
	const handler = getWindowHandler(appWindow)

	// track state of window as maximized/windowed
	let isMaximized = false

	// make a definition for the window/full listener
	let resizeListener: any

	// make a manual store subscription
	$: appIcon = $windowTitle.icon
	$: appTitle = $windowTitle.title

	
	onMount(() => {
		resizeListener = window.addEventListener('resize', async () => {
			isMaximized = await appWindow.isMaximized();
		})
	})

	onDestroy(() => {
		window.removeEventListener('resize', resizeListener);
	})


</script>






<div class="titlebar flex h-10 px-2">

	<!-- Window Controls -->
	<div class="flex items-center text-lg">
		<IconButton btnTlwnd="justify-center items-center flex w-4 h-4 border mx-1 rounded-full text-xs bg-red-500 text-red-900 border-red-700 hover:bg-red-400 hover:border-red-500 hover:text-red-700" icon="material-symbols:close" on:click={handler.close} />
		
		<IconButton btnTlwnd="justify-center items-center flex w-4 h-4 border mx-1 rounded-full text-xs bg-yellow-400 text-yellow-900 border-yellow-600 hover:bg-yellow-200 hover:border-yellow-500 hover:text-yellow-700" icon="mdi:minimize" on:click={handler.minimize} />
		{#if !isMaximized}
			<IconButton btnTlwnd="justify-center items-center flex w-4 h-4 border mx-1 rounded-full text-xs bg-green-500 text-green-800 border-green-600 hover:bg-green-300 hover:border-green-500 hover:text-green-700" icon="majesticons:maximize" on:click={() => { handler.maximize(); isMaximized = true }} />
		{:else}
			<IconButton btnTlwnd="justify-center items-center flex w-4 h-4 border mx-1 rounded-full text-xs bg-blue-500 text-blue-800 border-blue-600 hover:bg-blue-300 hover:border-blue-500 hover:text-blue-700" icon="material-symbols:select-window" on:click={() => { handler.toggle(); isMaximized = false }} />
		{/if}

	</div>

	<div class="flex flex-col mx-2">

	</div>

	<!-- Drag Region -->
	<div data-tauri-drag-region class="flex flex-grow mt-1"></div>

	<!-- Window Title -->

	<div></div>

	<!--
	<div class="flex items-center select-none text-amber-400">
		<iconify-icon icon={appIcon} class="text-lg" />
		<span class="ml-2 text-sm">{appTitle}</span>
	</div>
	-->

	<!-- Drag Region -->
	<div data-tauri-drag-region class="flex flex-grow mt-1"></div>




</div>