<script>
  import Form from "./components/Form.svelte";

  function handleOnSubmit() {
    console.log("I'm the handleOnSubmit() in App.svelte");
  }
</script>

<main>
  <h1>Captive Portal</h1>
  <Form on:submit={handleOnSubmit} />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
