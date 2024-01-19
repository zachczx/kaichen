<script>
import anime from 'animejs';
import { onMount } from 'svelte';

    // Wrap every letter in a span
onMount(() => {
var textWrapper = document.querySelector('.ml2');
textWrapper.innerHTML = textWrapper.textContent.replace(/\S/g, "<span class='letter'>$&</span>");

anime.timeline({loop: true})
  .add({
    targets: '.ml2 .letter',
    scale: [4,1],
    opacity: [0,1],
    translateZ: 0,
    easing: "easeOutExpo",
    duration: 950,
    delay: (el, i) => 70*i
  }).add({
    targets: '.ml2',
    opacity: 0,
    duration: 1000,
    easing: "easeOutExpo",
    delay: 1000
  });
})
</script>

<h1 class="ml2">Kai loves his food.</h1>
<p class="text-3xl">Kai loves noodles. Soup cai cai. sausage. fishball. tomatoes. mushrooms, fungus, squid. He has also grown to like meat.</p>

<style>
.ml2 {
  font-weight: 900;

}

.ml2 .letter {
  display: inline-block;
  line-height: 1em;
}
</style>