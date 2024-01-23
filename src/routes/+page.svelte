<script>
import ProgressBar from '../components/ProgressBar.svelte';

//images
import Swing from '../components/Swing.svelte';

import toycars from '$lib/assets/nick-xcRt6KM5s04-unsplash_full.webp';
import classphoto from '$lib/assets/photo-output_full.webp';
import spiderwebbg from '$lib/assets/matthieu-joannon-QoX88h9Pzpw-unsplash_full.webp';
import spidermanicon from '$lib/assets/83074-spiderman-venom-youtube-symmetry-area-free-hq-image_resized.webp';
import venomicon from '$lib/assets/pngwing.com_resized.webp';
import milesicon from '$lib/assets/mileshead_resized.webp';

import fruitbackground from "$lib/assets/bruna-branco-7r1HxvVC7AY-unsplash.webp";
import icecreambackground from "$lib/assets/lama-roscu-Wpg3Qm0zaGk-unsplash.webp";
import noodlebackground from "$lib/assets/pexels-polina-tankilevitch-4518665.webp";

import Traffic from '../components/Traffic.svelte';

import Hello from '../components/Hello.svelte';

import FruitScroll from '../components/FruitScroll.svelte';

import Food from '../components/Food.svelte';

import IceCream from '../components/IceCream.svelte';

import Growing from '../components/Growing.svelte';

import Particles from '../components/Particles.svelte';

import { onMount } from 'svelte';
//bootstrap icons

import HeartFill from "svelte-bootstrap-icons/lib/HeartFill.svelte";
import Apple from "$lib/assets/svg/apple.svg";
    
//---------------------------
    
onMount(() => {
    let observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
            console.log(entry)
            if (entry.isIntersecting) {
                entry.target.classList.add('show')               
            } else {
                entry.target.classList.remove('show')
            }
        })
    })
const hiddenElements = document.querySelectorAll('.hide')
hiddenElements.forEach((el) => observer.observe(el))

})

let spiderhead = 0
function clickSpidey() {
    spiderhead += 1
}
</script>
<Particles />
<ProgressBar />
<main>
<section class="bg-sky-500">
    <div class="hide grid content-center justify-items-center text-white pt-6 px-4">
        <Growing />
    </div>
</section>
    
<section style="background-image:url('{spiderwebbg}'); background-size: cover; background-position: 70%;" class="bg-red-500">
    <div class="hide text-white grid content-end justify-items-center px-8 py-5">
        <h1 class="mb-5">Kai loves Spiderman.</h1>
        <div class="text-3xl flex items-center"><HeartFill width={20} height={20} fill="red" /><HeartFill width={20} height={20} fill="red" /><HeartFill width={20} height={20} fill="red" class="me-2" />Peter Parker<button on:click={clickSpidey}><img alt='Spidey' src={spidermanicon} width='80' height='80' class="self-center ms-4"></button> 
            <span class="text-red-500 flex">
                {#if spiderhead > 0 && spiderhead <= 10}
                x{spiderhead} <span class="self-center ms-2"><HeartFill width={20} height={20} /></span>
                {:else if 10 < spiderhead && spiderhead <= 20 }
                x{spiderhead}<span class="flex self-center ms-2"><HeartFill width={20} height={20} /></span><span class="flex self-start"><HeartFill width={20} height={20} /></span><span class="flex self-end"><HeartFill width={30} height={30} /></span>
                {:else if 20 < spiderhead && spiderhead <= 30}
                x{spiderhead}<span class="flex self-center ms-2"><HeartFill width={20} height={20} /></span><span class="flex self-start"><HeartFill width={20} height={20} /></span><span class="flex self-end"><HeartFill width={30} height={30} /></span><span class="flex self-start"><HeartFill width={40} height={40} /></span><span class="flex self-center ms-2"><HeartFill width={35} height={35} /></span>
                {:else if spiderhead > 30}
                x{spiderhead}<span class="flex self-center ms-2"><HeartFill width={20} height={20} /></span><span class="flex self-start"><HeartFill width={20} height={20} /></span><span class="flex self-end"><HeartFill width={30} height={30} /></span><span class="flex self-start"><HeartFill width={40} height={40} /></span><span class="flex self-center ms-2"><HeartFill width={35} height={35} /></span><span class="flex self-start"><HeartFill width={60} height={60} /></span><span class="flex self-end"><HeartFill width={45} height={45}/></span>
                {/if}
            </span>
        </div>

        <div class="text-3xl flex items-center">
            <HeartFill width={20} height={20} fill="red" /><HeartFill width={20} height={20} fill="red" class="me-2" />Venom<img alt='Spidey' src={venomicon} width='80' height='80' class="self-center ms-4">
        </div>
        <div class="text-3xl flex items-center">
            <HeartFill width={20} height={20} fill="red" class="me-2" />Miles (a bit)<img alt='Spidey' src={milesicon} width='80' height='80' class="self-center ms-4">
        </div>
        <div class="flex place-content-end">
            <Swing />        
        </div>
    </div>
</section>
    
<section style="background-image:url('{toycars}'); background-position: 90% 10%; background-size: cover;">
    <div class="hide">
        <Traffic />
        <div class="grid content-center justify-items-center text-white pt-6 px-4">
            <h1 class="text-white">Kai likes vehicles.</h1>
            <p class="text-3xl text-white">Cars. Taxis. Police cars. Fire trucks. Excavators. Buses. </p>
        </div>
    </div>
</section>
    
<section style="background-image:url('{icecreambackground}'); background-position: 50% 50%; background-size: cover;" class="bg-orange-300">
    <IceCream />
</section>
    
<section style="background-image:url('{fruitbackground}'); background-position: 50% 50%; background-size: cover;">
    <div class="hide grid content-center justify-items-center text-white pt-6 px-4">
    <h1 class="inline">Kai enj<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-apple fill-red-600 hover:fill-red-400 inline" width="80" height="80" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
            <path d="M12 14m-7 0a7 7 0 1 0 14 0a7 7 0 1 0 -14 0" />
            <path d="M12 11v-6a2 2 0 0 1 2 -2h2v1a2 2 0 0 1 -2 2h-2" />
            <path d="M10 10.5c1.333 .667 2.667 .667 4 0" />
        </svg>ys fruit.</h1>
    <p class="text-3xl mt-4 mb-7">Grapes. Apples. Strawberries. Blueberries. Watermelons. Oranges. Pineapples.</p>
        <FruitScroll />
    </div>
</section>
    
<section class="bg-sky-500" style="background-image:url('{noodlebackground}'); background-position: 50% 50%; background-size: cover;">
    <div class="hide grid content-center justify-items-center text-white pt-6 px-4">
        <Food />
    </div>
</section>

<section style="background-image:url('{classphoto}'); background-size: cover; background-position: 80% 70%;" class="bg-yellow-300">
    <div class="hide grid content-center justify-items-center text-white">
        <Hello />  
    </div>
</section>

</main>
