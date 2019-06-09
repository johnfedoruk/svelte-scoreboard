<script>
  let player = {
    name: "",
    points: 0,
  }
</script>

<form>
  <input type="text" placeholder="Name" bind:value={player.name}>
  <input type="number" placeholder="Points" bind:value={player.points}>
  <input type="submit" value="Add Player" >
</form>