<script>
    import Card from "./Card.svelte"

    let { posts = [] } = $props()
</script>

<div class="TimeLine">
    <div class="TimeLine-continer">
      {#each posts as post }
        <Card {...post} />
      {:else}
        <p>Loading...</p>
      {/each}
    </div>
</div>

<style>
  .TimeLine {
    padding: 4em 0 0 0;
  }
</style>