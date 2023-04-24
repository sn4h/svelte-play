<script>
    import ArtistList from "../ArtistList.svelte";
    import ArtistSearch from "../ArtistSearch.svelte";

    let searchTerm = "hllo world";
    let artistList = [
        {
            name: "Hans",
            reknown: "testing"
        },{
            name: "Philip",
            reknown: "testing"
        },{
            name: "Joachim",
            reknown: "testing"
        }
    ]
</script>

<ArtistSearch {searchTerm} />
<ArtistList {artistList} />