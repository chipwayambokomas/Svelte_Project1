<script>
  import Card from "./lib/Card.svelte"
  let name = "Saul"
  let title = "My name"
  let toDo = ""
  let checked = false;
  function onClick(){
    count++;

    list.push(toDo)
    toDo=""
    list = list;
  }
  let count = 0;
  let list = [
   
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
<input type="text" bind:value={toDo}/>
<input type="checkbox" bind:checked/>
<button on:click={onClick}>Click me</button>

{#each list as toDo}
<Card>{toDo}</Card>
{/each}
<style>

  .div1{
    display: flex;
  }

</style>