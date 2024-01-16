<script>
  const formValues = {
    name: '',
  }
</script>

<main>
  <div>
    <pre>
      {JSON.stringify(formValues, null, 2)}
    </pre>
  </div>
  <form>
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" bind:value={formValues.name}>
    </div>
  </form>
</main>

<style>
  
</style>
