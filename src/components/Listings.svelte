<script>
    export let todos;
</script>

<ul>
    {#each todos as todo}
        <li>{ todo.title }</li>
    {/each}
</ul>
