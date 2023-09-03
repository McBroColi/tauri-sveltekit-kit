

<script lang='ts'>
	import { setContext } from "svelte"
	import type { ClassData } from "./ButtonType";

	export let thisClass: string = ""

	export let iClass: string = ""
	export let tClass: string = ""
	export let sClass: string = ""
	
	const classData: ClassData = {iClass, tClass, sClass}
	setContext('buttonClassData', classData)
</script>





<div class="{thisClass}">
	<slot />
</div>