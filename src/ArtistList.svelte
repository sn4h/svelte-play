<script>
    export let artistList;
</script>

{#each artistList as {title, body}}
<div class="artist">
    <h2>{title}</h2>
    <p>{body}</p>
</div>   
{:else}
    <span>No data</span>
{/each}

<style>
.artist {
    margin-bottom: 0.5em;
    border-bottom: 1px grey;
}
</style>
