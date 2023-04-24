<script>
    export let list;
</script>

{#each list as {title, body}}
<div class="artist">
    <h2>{title}</h2>
    <p>{body}</p>
</div>   
{:else}
    <span>No data</span>
{/each}

<style>
.artist {
    margin: 0.5rem 0;
    padding-bottom: 0.5rem;
    border-bottom: 1px grey solid;
}
</style>
