<script>
    import Card from './Card.svelte';
    import Filters from './Filters.svelte';

    export let todos;
    export let filteredContent = todos;

    function filterData(event) {
        // Show all data
        if (event.detail === 'all') {
            filteredContent = todos;
        // Only show completed items
        } else if (event.detail === 'complete') {
            filteredContent = todos.filter(item => item.completed);
        // Only show incomplete items
        } else {
            filteredContent = todos.filter(item => !item.completed);
        }
    }
</script>

<Filters on:updatefilter={ filterData } />

<ul>
    {#each filteredContent as todo}
        <Card data={ todo } />
    {/each}
</ul>
