<script>
import firetruck from '$lib/assets/_89a7c601-7ead-4e09-aef0-48325c78f215.webp';
import CircleFill from "svelte-bootstrap-icons/lib/CircleFill.svelte";
import { onMount } from 'svelte';
import anime from 'animejs';

onMount(() => {

	let animation_car = anime({
		targets: '.firetruck',
		translateX: -1000,
		direction: 'alternate',
		autoplay: false,
		loop: 1,
		easing: 'easeInOutQuad',
		duration: 2000,
	})
	document.getElementById('move-car').addEventListener("click", animation_car.play)
	document.getElementById('stop-car').addEventListener("click", animation_car.pause)
})

</script>

<div class="grid justify-items-end">
	<img class="firetruck me-5 " src={firetruck} alt="Wee woo wee woo222" >
</div>
<div class="flex justify-center">
	<div class="flex justify-between border-4 border-gray-400 space-x-3 rounded-lg bg-black p-3">
	<button id="move-car" class="flex space-x-3">
		<CircleFill fill="limegreen" width="40" height="40" />
		<CircleFill fill="yellow" width="40" height="40" />
	</button>
	<button id="stop-car">
		<CircleFill fill="red" width="40" height="40" />
	</button>
	</div>
</div>


