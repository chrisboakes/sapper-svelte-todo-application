<script>
	import { slide } from 'svelte/transition';
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
    {#each filteredContent as todo (todo.id)}
        <li transition:slide>
			<Card data={ todo } />
		</li>
    {/each}
</ul>
