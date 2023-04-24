<script>
    export let artistList;
    let name = "Hans";
    let rekon = 'testing';
</script>

{#each artistList as {name, reknown}}
<div class="container">
    <h2>{name}</h2>
    <p>{reknown}</p>
</div>   
{/each}
