<script>
import icecreampic from "$lib/assets/20230527_194706.webp";
import icecreampic2 from "$lib/assets/20230708_201806.webp";
import icecreampic3 from "$lib/assets/20230916_193540.webp";
import icecreampic4 from "$lib/assets/20231216_150032.webp";
import icecreampic5 from "$lib/assets/PXL_20231022_102535539.webp";
import icecreampic6 from "$lib/assets/PXL_20231231_122645070.webp";
import { onMount } from "svelte";

import anime from 'animejs';

onMount(() => {

    let pics = document.querySelectorAll('.animate')

    pics.forEach(el => {
        el.addEventListener('mouseenter', () => {
            console.log('entered!')
            let animation = anime.timeline({
                targets: el,
                duration: 500,
            });
            animation
            .add({
                scale: 1.5,
                translateZ: 900,
                easing: 'easeInCubic',
                zIndex: 3,
            })
            .add({

            });
        });

        el.addEventListener('mouseleave', () => {
            console.log('left!')
            anime({
                targets: el,
                scale: 1,
                duration: 500,
                zIndex: -1,
            })
        });
    })

    let textWrapper = document.querySelector('ml2')
    console.log(textWrapper)
    textWrapper.innerHTML = textWrapper.textContent.replace(/\S/g, '<span class="letter">$&</span>')

    anime.timeline({loop: true})
        .add({
            targets: '.ml2',
            easing: "easeOutExpo",
            duration: 300,
            delay: (el, i) => 70*i,
        });

});
</script>
<div class="hide max-h-full grid content-center justify-items-center text-white pt-6 px-4">
    <h1 class="ml2 mb-2">Kai eats junk food sometimes.</h1>
    <p class="text-3xl mb-4">Ice cream, ice cream, and ice cream. And milo, orange juice, honey lemon.</p>

<div class="container max-h-min mx-auto grid grid-cols-2 md:grid-cols-6 grid-flow-row auto-rows-max gap-6 mt-5">
    <div class="bg-white border-x-2 border-t-2 border-b-8 border-white overflow-hidden"><div class="mb-5 overflow-hidden"><img src={icecreampic} alt="Yum" class="object-scale-down animate" loading="lazy"></div></div>
    <div class="bg-white border-x-2 border-t-2 border-b-8 border-white overflow-hidden"><div class="mb-5 overflow-hidden"><img src={icecreampic2} alt="Yum" class="object-scale-down animate" loading="lazy"></div></div>
    <div class="bg-white border-x-2 border-t-2 border-b-8 border-white overflow-hidden"><div class="mb-5 overflow-hidden"><img src={icecreampic3} alt="Yum" class="object-scale-down animate" loading="lazy"></div></div>
    <div class="bg-white border-x-2 border-t-2 border-b-8 border-white overflow-hidden"><div class="mb-5 overflow-hidden"><img src={icecreampic4} alt="Yum" class="object-scale-down animate" loading="lazy"></div></div>
    <div class="bg-white border-x-2 border-t-2 border-b-8 border-white overflow-hidden"><div class="mb-5 overflow-hidden"><img src={icecreampic5} alt="Yum" class="object-scale-down animate" loading="lazy"></div></div>
    <div class="bg-white border-x-2 border-t-2 border-b-8 border-white overflow-hidden"><div class="mb-5 overflow-hidden"><img src={icecreampic6} alt="Yum" class="object-scale-down animate" loading="lazy"></div></div>
</div>
</div>

<style>
.animate:before {
    z-index: -1;
}
</style>