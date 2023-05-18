<script>
  import Card from "./lib/Card.svelte"
  let name = "Saul"
  let title = "My name"
</script>

<h1 title={title}>Hello {name}</h1>

<div class="div1">
  <Card/>
<Card title="Different">
  <h1>Hello World</h1>
</Card>
</div>


<style>

  .div1{
    display: flex;
  }

</style>