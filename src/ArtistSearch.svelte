<script>
export let searchTerm;
</script>

<div class="SearchForm">
    <h4>
        Search:
        <small>
            for:
            {searchTerm}
        </small>
    </h4>
    <div class="SearchInput">
        <input 
            type="text"
            aria-label="Search Input"
            bind:value={searchTerm}
        /> 
    </div>
</div>