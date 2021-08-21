<script context="module">
  import { apiURL } from "./../shared/ApiConfig.svelte";

  export function post(data) {
    const options = {
      method: "POST",
      body: JSON.stringify({ data }),
      headers: {
        "Content-Type": "application/json",
      },
    };
    console.log(data);
    fetch(apiURL, options)
      .then((res) => res.json())
      .then((res) => console.log(res));
  }
</script>
