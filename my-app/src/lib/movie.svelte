
<script>
    export let Title,Poster,Year
</script>
<style>
    article{
        border: 1 px solid black;
        border-radius: 4px;
        margin-bottom: 4px;
        padding:16px;


    }
    h3{
        font-size: 24px;
        margin-bottom:4px;
        }
</style>
<article>
<img alt={Title} src={Poster}/>
<h3>{Title}</h3>
<span>{Year}</span>
{#if 2020 - Year < 5}
<i>new</i>
{/if}
</article>
