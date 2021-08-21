<script>
  import { post } from "../services/Api.svelte";

  let user = {
    name: "",
    email: "",
    phoneNumber: "",
  };
  let checked = {
    email: false,
    terms: false,
  };

  function submit() {
    validate();
    post(user);
  }

  function validate() {
    console.log("I'm the validate() function");
  }
</script>

<form on:submit|preventDefault={submit}>
  <label>Name <input bind:value={user.name} /></label>
  <label>Email <input bind:value={user.email} /></label>
  <label>Phone <input bind:value={user.phoneNumber} /></label>
  <label>
    <input type="checkbox" checked={checked.email} />
    Yes! Send me regular email spam
  </label>

  <label>
    <input type="checkbox" checked={checked.terms} />
    Yes! I accept terms&conditions
  </label>

  <button type="submit"> Confirm </button>
</form>
