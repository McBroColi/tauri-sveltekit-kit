
<script>
    import '$styles/tailwind.css'
	import '$styles/app.css'
    import 'iconify-icon'
	import Appbar from '$components/app/Appbar.svelte'


</script>



<style>



</style>


<div class="w-screen h-screen relative flex flex-col bg-zinc-900 text-zinc-300 overflow-hidden">
	
	<div class="w-screen h-screen absolute gradient-bg pointer-events-none -z-50"></div>
	
	<Appbar />
	<slot />
</div>

