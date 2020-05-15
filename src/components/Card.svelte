<script>
    export let data;
</script>

<div class="card">
    <span class="status">
        {#if data.completed}
            <svg width="20" height="20" xmlns="http://www.w3.org/2000/svg"><path d="M10 19.993c5.523 0 10-4.474 10-9.993C20 4.48 15.523.007 10 .007S0 4.48 0 10c0 5.52 4.477 9.993 10 9.993z" fill="#32BEA6"/><path d="M9.198 15.316L4.47 11.632l1.344-1.725 2.904 2.262 4.792-6.915L15.308 6.5l-6.11 8.816z" fill="#fff"/></svg>
        {:else}
            <svg width="20" height="20" xmlns="http://www.w3.org/2000/svg"><path d="M10 0C4.486 0 0 4.486 0 10s4.486 10 10 10 10-4.486 10-10S15.514 0 10 0z" fill="#F44336"/><path d="M13.682 12.504a.833.833 0 11-1.178 1.178L10 11.178l-2.504 2.505a.83.83 0 01-1.179 0 .833.833 0 010-1.179L8.822 10 6.317 7.496a.833.833 0 111.179-1.179L10 8.822l2.504-2.505a.833.833 0 111.178 1.179L11.178 10l2.504 2.504z" fill="#FAFAFA"/></svg>
        {/if}
    </span>
    <span class="title { data.completed ? 'completed' : '' }">{ data.title }</span>
</div>

<style>
    .card {
        align-items: flex-start;
        display: flex;
        margin-bottom: .5rem;
        line-height: 1.2;
        justify-content: center;
    }

    .status {
        margin-right: 10px;
    }

    .title {
        width: 300px;
    }

    .completed {
        color: #666;
        text-decoration: line-through;
    }
</style>
