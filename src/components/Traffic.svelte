<script>
import { fly, fade } from 'svelte/transition'; 
import firetruck from '$lib/assets/_89a7c601-7ead-4e09-aef0-48325c78f215.webp';
import CircleFill from "svelte-bootstrap-icons/lib/CircleFill.svelte";
let visible = true
function visibleClick(color) {
	if (visible == true) {
		visible = false
	} else {
		visible = true
	}
}
</script>
<div class="flex justify-center"><button on:click={visibleClick}><CircleFill fill="green" width="40" height="40" /><CircleFill fill="yellow" width="40" height="40" /><CircleFill fill="red" width="40" height="40" /></button></div>
<div class="flex justify-end min-h-50">
{#if visible}
<img transition:fly={{duration:8000, x:-2000, opacity:1}} src={firetruck} alt="Wee woo wee woo" class="flex justify-end">
{/if}
</div>

