<script>
    import Card from './Card.svelte';
	import Filters from './Filters.svelte';

	export let todos;

	const filters = {
		all: () => true,
		complete: ({ completed }) => completed,
		incomplete: ({ completed }) => !completed
	};

	let selected = 'all';
	$: filteredContent = todos.filter(filters[selected]);
</script>

<Filters bind:selected />

<ul>
    {#each filteredContent as todo}
        <Card data={ todo } />
    {/each}
</ul>
