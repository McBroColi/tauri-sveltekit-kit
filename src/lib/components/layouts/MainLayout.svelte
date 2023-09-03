


<div class="flex flex-col px-2 h-full">
	<div class="w-full flex-grow">
		<slot />
	</div>
	
	{#if $$slots.notifbar}
		<div class="w-full h-6 flex flex-none items-center my-2 text-sm text-zinc-600">
			<slot name="notifbar" />
		</div>
	{:else}
		<div class="h-2 w-full"></div>
	{/if}
</div>