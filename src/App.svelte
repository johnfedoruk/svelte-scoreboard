<script>
  import Navbar from "./Navbar.svelte";
  import Player from "./Player.svelte";
  import AddPlayer from "./AddPlayer.svelte";

  let players = [
    {
      name: "John Doe",
      points: 50
    },
    {
      name: "Sam Doe",
      points: 15
    }
  ];

  const addPlayer = e => {
    players = [...players, e.detail];
  };

  const deletePlayer = index => {
    players = players.filter((_v, i) => i !== index);
  };
</script>

<style>

</style>

<Navbar />

<AddPlayer on:addPlayer={addPlayer} />

<div>
  {#if players.length === 0}
    <p>No players</p>
  {:else}
    {#each players as player, index}
      <Player
        name={player.name}
        points={player.points}
        on:deletePlayer={() => deletePlayer(index)} />
    {/each}
  {/if}
</div>
