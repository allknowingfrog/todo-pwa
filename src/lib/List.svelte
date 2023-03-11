<script>
  let items = JSON.parse(localStorage.getItem("items")) || []
  let new_item = ""

  const store = () => {
    items.push(new_item)
    items = items
    localStorage.setItem("items", JSON.stringify(items))

    new_item = ""
  }

  const remove = index => {
    items.splice(index, 1)
    items = items
    localStorage.setItem("items", JSON.stringify(items))
  }
</script>

<input bind:value={new_item}>

<button on:click={store}>Add</button>

<ul>
  {#each items as item, index}
    <li>{item}
      <button on:click={() => remove(index)}>Remove</button>
    </li>
  {/each}
</ul>
