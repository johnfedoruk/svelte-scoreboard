<script>
  export let name;
  export let points;
  let show_controls = false;
  const addPoint = () => {
    points += 1;
  };
  const removePoint = () => {
    points -= 1;
  };
  const showControls = () => {
    show_controls = !show_controls;
  }
</script>

<style>
  h1 {
    color: purple;
  }
  .show-controls {
    color: black;
    cursor: pointer;
    width: 30px;
    display: inline-block;
    text-align: center;
  }
</style>

<div>
  <h1>
     {name}
    <span on:click={showControls} class="show-controls">{#if show_controls}-{:else}+{/if}</span>
  </h1>
  <h3>{points || 0}</h3>
  {#if show_controls}
    <button on:click={addPoint}>+1</button>
    <button on:click={removePoint}>-1</button>
    <input type="number" bind:value={points} />
  {/if}
</div>
