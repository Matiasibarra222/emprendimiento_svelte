<script>
  import Card from "./Card.svelte";
  export let posts = []
</script>


<!-- TimeLine.svelte -->


<style>
  .TimeLine {
    padding: 4em 0 0 0;
  }
  .TimeLine-container{
    display: grid;
    grid-template-columns: 50% 50%;
    grid-gap:5px;
  }
</style>


<div class="TimeLine">
  <div class="TimeLine-container">
    {#each posts as post}
      <Card {...post} />
    {:else}
      <p> Loading... </p>
    {/each}

  </div>
</div>
