<script lang="ts">
    type mushroom = {
        name: string;
        rating: number;
    };
    let tired = false;
    let mushrooms: mushroom[] = [
        {
            name: "shiitake",
            rating: 4,
        },
        {
            name: "button",
            rating: 3,
        },
        {
            name: "crimini",
            rating: 2,
        },
    ];
    function handleClick() {
        mushrooms = mushrooms.slice(1);
    }
    async function giveAnswer() {
        throw new Error('I don\'t know');
    }
    const answer = giveAnswer();
</script>

{#if tired}
    <p>I'm tired</p>
{:else}
    <p>I'm not tired</p>
{/if}
<button on:click={handleClick}> remove mushrooom </button>
<p>keyed each block</p>
{#each mushrooms as mushroom, i (mushroom.name)}
    <h2>{i}. {mushroom.name} rating: {mushroom.rating}</h2>
{/each}
{#await answer}
<p>The answer is...</p>
{:then value}
<p>the answer is {value}!</p>
{:catch err}
<p>there is no answer. Reason: {err.message}</p>
{/await}
<style>
    p {
        font-size: x-small;
    }
</style>
