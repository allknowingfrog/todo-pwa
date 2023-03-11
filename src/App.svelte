<script>
  import List from './lib/List.svelte'
</script>

<main>
  <div>
    <img src="/checkmark.svg" class="logo" alt="Checkmark Logo" />
  </div>
  <h1>To Do</h1>

  <div class="card">
    <List />
  </div>
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
