<script>
import anime from 'animejs';
import { onMount } from 'svelte';
import HeartFill from "svelte-bootstrap-icons/lib/HeartFill.svelte";

    // Wrap every letter in a span
onMount(() => {
let foodTextWrapper = document.querySelector('.animatefoodheader');
foodTextWrapper.innerHTML = foodTextWrapper.textContent.replace(/\S/g, "<span class='foodletter'>$&</span>");

anime.timeline({loop: true})
  .add({
    targets: '.animatefoodheader .foodletter',
    scale: [4,1],
    opacity: [0,1],
    translateZ: 0,
    easing: "easeOutExpo",
    duration: 950,
    delay: (el, i) => 70*i
  }).add({
    targets: '.animatefoodheader',
    opacity: 0,
    duration: 100,
    easing: "easeOutExpo",
    delay: 50
  });
})
</script>

<h1 class="animatefoodheader">Kai loves his food.</h1>
<p class="text-3xl">Kai <HeartFill class="inline" fill="red" width={24} height={24} /> noodles. Soup cai cai. sausage. fishball. tomatoes. mushrooms, fungus, squid. He has also grown to like meat.</p>

<div class="mt-5">
<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-mushroom fill-orange-300 hover:fill-orange-400 stroke-orange-500 w-48 h-48 inline" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M20 11.1c0 -4.474 -3.582 -8.1 -8 -8.1s-8 3.626 -8 8.1a.9 .9 0 0 0 .9 .9h14.2a.9 .9 0 0 0 .9 -.9z" /><path d="M10 12v7a2 2 0 1 0 4 0v-7" /></svg>
<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-soup fill-white hover:fill-slate-200 stroke-gray-400 w-48 h-48 inline" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M4 11h16a1 1 0 0 1 1 1v.5c0 1.5 -2.517 5.573 -4 6.5v1a1 1 0 0 1 -1 1h-8a1 1 0 0 1 -1 -1v-1c-1.687 -1.054 -4 -5 -4 -6.5v-.5a1 1 0 0 1 1 -1z" /><path d="M12 4a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2" /><path d="M16 4a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2" /><path d="M8 4a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2" /></svg>
<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-sausage fill-rose-300 hover:fill-rose-400 stroke-rose-500 w-48 h-48 inline" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M5.5 5.5a2.5 2.5 0 0 0 -2.5 2.5c0 7.18 5.82 13 13 13a2.5 2.5 0 1 0 0 -5a8 8 0 0 1 -8 -8a2.5 2.5 0 0 0 -2.5 -2.5z" /><path d="M5.195 5.519l-1.243 -1.989a1 1 0 0 1 .848 -1.53h1.392a1 1 0 0 1 .848 1.53l-1.245 1.99" /><path d="M18.482 18.225l1.989 -1.243a1 1 0 0 1 1.53 .848v1.392a1 1 0 0 1 -1.53 .848l-1.991 -1.245" /></svg>
</div>
<style>
.animatefoodheader {
  font-weight: 900;
}

.animatefoodheader .foodletter {
  display: inline-block;
  line-height: 1em;
}
</style>