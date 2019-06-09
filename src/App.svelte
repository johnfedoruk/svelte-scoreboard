<script>
  import Navbar from "./Navbar.svelte";
  import Player from "./Player.svelte";

  let players = [

  ];
</script>

<style>

</style>

<Navbar />
<div>
  {#if players.length === 0}
    <p>No players</p>
  {:else}
    {#each players as player}
      <Player />
    {/each}
  {/if}
</div>
