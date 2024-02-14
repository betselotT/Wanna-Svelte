<script>
  const formValues = {
    name: '',
    profile: '',
    country: '',
    jobLocation: [],
    remoteWork: false,
    skillSet: [],
  }
  const name = 'Aman';

  function submitForm(event) {
    console.log(formValues);
  }
</script>

<main>
  <div>
    <pre>
      {JSON.stringify(formValues, null, 2)}
    </pre>
  </div>
  <form on:submit|preventDefault={submitForm}>
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" bind:value={formValues.name}>
    </div>

    <div>
      <label for="profile">Profile Summary</label>
      <textarea id="profile" bind:value={formValues.profile}></textarea>
    </div>

    <div>
      <label for="country">Country</label>
      <select id="country" bind:value={formValues.country}>
        <option value="">Select a Country</option>
        <option value="Ethiopia">Ethiopia</option>
        <option value="France">France</option>
        <option value="America">America</option>
      </select>
    </div>
    
    <div>
      <label for="job-location">Job Location</label>
      <select id="job-location" bind:value={formValues.jobLocation} multiple>
        <option value="Ethiopia">Ethiopia</option>
        <option value="France">France</option>
        <option value="America">America</option>
      </select>
    </div>

    <div>
      <input type="checkbox" id="remotework" bind:checked={formValues.remoteWork}>
      <label for="remotework">Open to remote work?</label>
    </div>

    <div>
      <label for="skillset">Skills?</label>
      <input type="checkbox" id="html" value="html" bind:group={formValues.skillSet}>
      <label for="html">HTML</label>
      <input type="checkbox" id="css" value="css" bind:group={formValues.skillSet}>
      <label for="css">CSS</label>
      <input type="checkbox" id="js" value="js" bind:group={formValues.skillSet}>
      <label for="js">JS</label>
    </div>
    
    <div>
      <button>Submit</button>
    </div>
  </form>

  <h3>Hello {name}</h3>
</main>

<style>
  
</style>
