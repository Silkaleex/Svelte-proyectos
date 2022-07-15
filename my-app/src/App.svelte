<script>
// @ts-nocheck
  import Input from "./lib/input.svelte"
</script>
<style>
  *{
    margin:0px;
    padding:0px;
    font-family:Georgia, 'Times New Roman', Times, serif;
  }
  body{
    background: linear-gradient(#A2C5FE,#C2E9FC);
    padding:40px;
    border:5px solid #D0DAE0
  }
  h1{
    font-size:32px;
    padding:25px;
    letter-spacing:3px;
  }
  section{
    align-items: center;
    display:flex;
    flex-direction:column;
  
  }
</style>
<body>
<section>
  <h1>Search Movies</h1>
  <Input/>
</body>