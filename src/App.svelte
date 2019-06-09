<script>
  import Navbar from "./Navbar.svelte";
  import Player from "./Player.svelte";

  let players = [
    {
      name: "John Doe",
      points: 50,
    },
    {
      name: "Sam Doe",
      points: 15,
    },
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
      <Player name={player.name} points={player.points} />
    {/each}
  {/if}
</div>
