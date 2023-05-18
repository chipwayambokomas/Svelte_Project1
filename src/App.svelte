<script>
  import Card from "./lib/Card.svelte"
  let name = "Saul"
  let title = "My name"
  let titleNew = ""
  let checked = false;
</script>

<h1 title={title}>{titleNew}</h1>
{#if checked}
<div class="div1">
  <Card/>
<Card title="Different">
  <h1>Hello World</h1>
</Card>
</div>

{:else}
<div>Check the checkbox to show the cards</div>
{/if}
<input type="text" bind:value={titleNew}/>
<input type="checkbox" bind:checked/>

<style>

  .div1{
    display: flex;
  }

</style>