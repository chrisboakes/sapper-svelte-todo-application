<script>
    import Card from './Card.svelte';
    import Filters from './Filters.svelte';

    export let todos;

    function filterData(event) {
        console.log(event.detail);
    }
</script>

<Filters on:updatefilter={ filterData } />

<ul>
    {#each todos as todo}
        <Card data={ todo } />
    {/each}
</ul>
