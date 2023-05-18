<script lang="ts">
    export let title = "Normal title";
    let checked = false;
</script>

<div class:completed={checked}>
    <span> <slot/></span>
 

  <input type="checkbox" bind:checked/>

</div>

<style>
    div{
        background-color: aqua;
        padding: 1rem;
        border-radius: 2px;
        margin: 1rem;
        min-width: 10rem;
    }

    .completed{
        text-decoration: line-through;
        background-color: gray;
    }
</style>
