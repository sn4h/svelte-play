<script>
    import {createEventDispatcher} from 'svelte';

    const dispatch = createEventDispatcher();
    export let searchTerm;
</script>

<div class="SearchForm">
    <h4>
        Search:
        <small>
            {#if searchTerm}
                for:
            {/if}
            {searchTerm}
        </small>
    </h4>
    <div class="SearchInput">
        <input
                type="text"
                aria-label="Search Input"
                bind:value={searchTerm}
                on:keyup={() => {
                dispatch('updateSearch');
            }}
        />
    </div>
</div>