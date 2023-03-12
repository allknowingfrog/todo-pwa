<script>
  import List from './lib/List.svelte'
  import FetchDemo from './lib/FetchDemo.svelte'

  let testMode = false
</script>

<main>
  <div>
    <img src="/checkmark.svg" class="logo" alt="Checkmark Logo" />
  </div>
  <h1>To Do</h1>

  <div>
    <input type="checkbox" name="testMode" bind:checked={testMode}>
    <label for="testMode">Test Mode</label>
  </div>

  {#if testMode}
    <div class="card">
      <FetchDemo />
    </div>
  {:else}
    <div class="card">
      <List />
    </div>
  {/if}
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
</style>
