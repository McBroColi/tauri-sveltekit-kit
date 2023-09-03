

<script lang='ts'>
	import type { ClassData } from "./ButtonType"
	import { getContext } from "svelte"

	export let icon: string
	export let text: string | undefined = undefined
	export let subtext: string | undefined = undefined

	const { iClass, tClass, sClass }: ClassData = getContext('buttonClassData')





</script>



<button class="flex flex-col">
	<div class="flex items-center justify-center w-full">
		<iconify-icon class="{iClass}" {icon} />
		{#if text}
			<p class="{tClass}">{text}</p>
		{/if}
	</div>
	{#if subtext}
		<p class="my-1 mx-auto {sClass}">{subtext}</p>
	{/if}
</button>