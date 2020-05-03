<script>
    import Card from './Card.svelte';

    export let todos;
</script>

<ul>
    {#each todos as todo}
        <Card data={ todo } />
    {/each}
</ul>
