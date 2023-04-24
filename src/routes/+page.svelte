<script>
    import {onMount} from "svelte"
    import ArtistList from "../ArtistList.svelte";
    import ArtistSearch from "../ArtistSearch.svelte";

    const endpoint = "https://jsonplaceholder.typicode.com/posts";
  
    let searchTerm = "hllo world";
    let artistList = [];

    onMount(
      async()  => {
        
        const response = await fetch(endpoint);
        artistList = await response.json();
        console.log(artistList);
}
    ) 
</script>

<ArtistSearch {searchTerm} />
<ArtistList {artistList} />