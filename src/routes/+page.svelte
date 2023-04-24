<script>
    import {onMount} from 'svelte'
    import ArtistList from '../ArtistList.svelte';
    import ArtistSearch from '../ArtistSearch.svelte';

    const endpoint = 'https://jsonplaceholder.typicode.com/posts';
  
    let searchTerm = '';
    let artistList = [];
    let displayList = [];

    onMount(async()  => {
        const response = await fetch(endpoint);
        artistList = await response.json();
        displayList = artistList;
     }) 

     function onFilterList(list, term) {
        return list.filter(item => {
            return (
                item.title.toLowerCase().match(term.toLowerCase()) ||
                item.body.toLowerCase().match(term.toLowerCase()) 
            );
        });
     }
</script>

<main>
    <ArtistSearch 
        bind:searchTerm
        on:updateSearch={() => {
            displayList = onFilterList(artistList, searchTerm);
        }}
    />
    <ArtistList bind:list={displayList} />
</main>

<style>
    main {
        max-width: 40rem;
        margin: 0 auto;
    }
</style>