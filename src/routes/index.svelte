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

<Listings todos={ data } />
