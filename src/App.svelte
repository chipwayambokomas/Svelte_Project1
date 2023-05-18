<script>
  import Card from "./lib/Card.svelte"
  let name = "Saul"
  let title = "My name"
  let titleNew = ""
  let checked = false;
  function onClick(){
    count++;

    list.push("Word")
    list = list;
  }
  let count = 0;
  let list = [
    "Hello",
    "You"
  ]
</script>

<h1 title={title}>Count: {count}</h1>
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
<button on:click={onClick}>Click me</button>

{#each list as word}
<h1>{word}</h1>
{/each}
<style>

  .div1{
    display: flex;
  }

</style>