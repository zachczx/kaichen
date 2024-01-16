<script>
import { fly } from 'svelte/transition'; 
import spiderman from '$lib/assets/_4f970765-bfa3-471a-9c40-b2fb8d3e5cb1.webp';
import spiderman200px from '$lib/assets/_4f970765-bfa3-471a-9c40-b2fb8d3e5cb1_200px.webp';
import venom from '$lib/assets/_16f0c0d3-4025-4397-bf59-2f3d26f17891.webp';
import venom200px from '$lib/assets/_16f0c0d3-4025-4397-bf59-2f3d26f17891_200px.webp';
import { quintIn } from 'svelte/easing';

export let venomMove = true
export function clickVenom() {
    if (venomMove == false) {
        venomMove = true
    } else {
        venomMove = false
    }
}

</script>
{#if venomMove == true}
<picture>
    <source media="(min-width:1440px)" srcset={spiderman}>
    <img src={spiderman200px} alt="Spidey" style="width:auto;" loading="lazy" transition:fly={{duration:1500, x:'-200%', y:'-200%', easing:quintIn, opacity:1}}>
</picture>
{/if}
<button on:click={clickVenom}>
    <picture>
        <source media="(min-width:1440px)" srcset={venom}>
        <img src={venom200px} alt="Venom" style="width:auto;" loading="lazy">
    </picture>
</button>

