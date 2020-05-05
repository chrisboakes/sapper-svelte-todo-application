<script>
    import Listings from '../components/Listings.svelte';
    
    export let data;
</script>

<script context="module">
    export async function preload() {
        const response = await this.fetch('https://jsonplaceholder.typicode.com/todos');
        const responseJson = await response.json();

		return {
			data: responseJson
		}
    }
</script>

<svelte:head>
	<title>Listings | Sapper/Svelte Demo</title>
	<meta name="description" content="Dummy sapper/svelte project - listings" />
</svelte:head>

<Listings todos={ data } />
