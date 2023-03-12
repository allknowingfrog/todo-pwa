<script>
  let todo = ""

  fetch('https://jsonplaceholder.typicode.com/todos/1')
    .then(response => response.json())
    .then(json => todo = JSON.stringify(json))
</script>

<div>
  <h1>Testing</h1>

  <p>{todo}</p>
</div>
