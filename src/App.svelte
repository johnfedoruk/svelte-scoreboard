<script>
  let name = "John Doe";
  let points = 100;
  const addPoint = () => {
    points += 1;
  }
  const removePoint = () => {
    points -= 1;
  }
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<div>
  <h1>{name}</h1>
  <h3>{points||0}</h3>
  <button on:click={addPoint}>+1</button>
  <button on:click={removePoint}>-1</button>
  <input type="number" bind:value={points}>
</div>
