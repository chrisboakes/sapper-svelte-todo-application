<script>
    export let selected = 'all';
</script>

<div>
	<label for="filter">Filter:</label>
    <select id="filter" bind:value={ selected }>
        <option value="all">All</option>
        <option value="incomplete">Incomplete</option>
        <option value="complete">Complete</option>
    </select>
</div>

<style>
	label {
		font-size: .8rem;
	}

    div {
        padding-bottom: 1.5rem;
        margin: 0 auto;
        width: 330px;
    }

    select {
        width: 100%;
    }
</style>
