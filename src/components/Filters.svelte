<script>
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();

    let selected = 'all';
    
    function updateFilter(event) {
        dispatch('updatefilter', selected);
    }
</script>

<style>
    div {
        padding-bottom: 1.5rem;
        margin: 0 auto;
        width: 330px;
    }

    select {
        width: 100%;
    }
</style>

<div>
    <select bind:value={ selected } on:change={ updateFilter }>
        <option value="all">All</option>
        <option value="incomplete">Incomplete</option>
        <option value="complete">Complete</option>
    </select>
</div>