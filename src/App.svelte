<script>
  import Card from "./lib/Card.svelte"
  let name = "Saul"
  let title = "My name"
  let titleNew = ""
</script>

<h1 title={title}>{titleNew}</h1>

<div class="div1">
  <Card/>
<Card title="Different">
  <h1>Hello World</h1>
</Card>
</div>
<input type="text" bind:value={titleNew}/>

<style>

  .div1{
    display: flex;
  }

</style>