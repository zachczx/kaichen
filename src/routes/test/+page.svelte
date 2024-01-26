<script>
    import { onMount } from 'svelte';

let data

onMount(async () => {
  const response = await fetch('https://rickandmortyapi.com/api/character/1,2,3')
  data = await response.json()
  console.log(data)
})

//async function getChar() {
//    const response2 = await fetch('https://rickandmortyapi.com/api/character/1,2,3,4,5,6')
//    individuals = await response2.json()
//    console.log(individuals)
//    if (response2.ok) {
//      return individuals
//    } else {
//      throw new Error(individuals)
//    }
//};


</script>

<main class="p-5">
<div class="text-center"><button>Click here</button></div>
<ul>



<hr>
{#if data}
  {#each data as individual}
  <p>{individual.id} - {individual.name}</p>
  <p><img src={individual.image} alt={individual.name}></p>
  {/each}
{:else}
<p>loading...</p>
{/if}

</ul>

</main>