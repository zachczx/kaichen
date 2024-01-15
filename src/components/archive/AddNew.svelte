<script>
import { flip } from "svelte/animate";
import { dndzone } from 'svelte-dnd-action';

let items = []
let person
let dept
let count = 0
$: rank = count + 1
let total
//let quotaBandA, quotaBandB, quotaBandC, quotaBandD

$: quotaBandA = Math.ceil(0.05 * total) 
$: quotaBandB = Math.ceil(0.45 * total) + quotaBandA
$: quotaBandC = Math.ceil(0.45 * total) + quotaBandB
$: quotaBandD = Math.ceil(0.05 * total) + quotaBandC


let addName = () => {
    items.push({id: rank, "person": person, "dept": dept})
    items = items
    console.log(items)
    count += 1
    console.log(quotaBandA)
    console.log(quotaBandB)
    console.log(quotaBandC)
    console.log(quotaBandD)
    console.log(total)
}

const flipDurationMs = 200;
function handleDndConsider(e) {
    items = e.detail.items;
    console.log('consider')
}
function handleDndFinalize(e) {
    items = e.detail.items;
}

</script>

<h2 class="mt-5 ">Add new</h2>
<div class="row mb-5">
    <label for="name" class="me-2">Name:</label><input type="text" class="border-2 rounded border-red-300 hover:border-slate-400" id="name" placeholder="Name" bind:value={person} />
    <label for="rank" class="me-2">Rank:</label><input type="number" class="border-2 rounded border-red-300 hover:border-slate-400" id="rank" placeholder="Rank" bind:value={rank} />
    <label for="dept" class="me-2">Dept:</label><input type="text" class="border-2 rounded border-red-300 hover:border-slate-400" id="dept" placeholder="Dept" bind:value={dept} />
    <button type="submit" class="rounded bg-red-600 px-3 py-1 text-white hover:bg-red-400 active:bg-red-800" on:click={addName}>Submit</button>
</div>

<input type="text" class="border-2 rounded border-red-300 hover:border-slate-400" id="total" placeholder="Total" bind:value={total} />

<div class="row">
<h2>Ranking List</h2>
<p>(Number of entries = {count})</p>
<section use:dndzone="{{items, flipDurationMs}}" on:consider="{handleDndConsider}" on:finalize="{handleDndFinalize}">
{#each items as item(item.id)}
    <div class="text-3xl bg-red-300 border border-red-300 rounded mb-7" animate:flip="{{duration: flipDurationMs}}">
        {#if item.id <= quotaBandA}
        <button class="rounded bg-green-300 px-3 py-1 hover:bg-green-400" on:click={addName}>Band 1</button>
        {:else if item.id > quotaBandA && item.id <= quotaBandB}
        <button class="rounded bg-yellow-300 px-3 py-1 hover:bg-yellow-400" on:click={addName}>Band 2</button>
        {:else if item.id > quotaBandB && item.id <= quotaBandC}
        <button class="rounded bg-blue-200 px-3 py-1 hover:bg-blue-300" on:click={addName}>Band 3</button>
        {:else if item.id > quotaBandC && item.id <= quotaBandD}
        <button class="rounded bg-neutral-900 text-white px-3 py-1 hover:bg-neutral-700" on:click={addName}>Band 4</button>
        {:else}
        <button class="rounded bg-gray-300 px-3 py-1 hover:bg-gray-400" on:click={addName}>N.A.</button>
        {/if}
        {item.id} - {item.person} - {item.dept}
    </div>
{/each}
</section>
</div>