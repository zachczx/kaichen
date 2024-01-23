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

<style>
.animatefoodheader {
  font-weight: 900;
}

.animatefoodheader .foodletter {
  display: inline-block;
  line-height: 1em;
}
</style>