<script>
    import Movie from "./movie.svelte";
    let value = ''
    let response = []
    const handleInput = (event) => value = event.target.value
    $:if(value.length > 2)
    {response = fetch(`https://www.omdbapi.com/?s=${value}&apikey=422350ff`)
.then(res => res.json())
.then(apiResponse => apiResponse.Search || [])
}
</script>
<input placeholder="search movies..."{value} on:input={handleInput}>
{#await response}
<strong>Loading...</strong>
{:then movies}
{#each movies as {Title,Poster,Year}}
<Movie 
Title={Title} 
Poster={Poster}
Year={Year}
/>
{:else}
<strong>No hay Resultados</strong>
{/each}
{/await}
<style>
    input{
        background-color: #E2EBF0;
        letter-spacing: 2px;
        font-size: 20px;
        padding:5px;
        
    }    
    strong{
        margin-top:20px;
        border:2px solid #06BCFB;
        padding:10px;
        background: linear-gradient(#96E4DF,#4DCCC6);
    }
</style>