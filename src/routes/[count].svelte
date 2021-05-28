<script>
  import { goto } from "$app/navigation";
  import { onDestroy, onMount } from "svelte";

  onMount(() => console.info("🧛 Count Mount!"));
  onDestroy(() => console.info("🧛 Count Destroy!"));

  let count = 0;

  function increment() {
    ++count;
    // ++count;

    goto(`/${count}`);
  }
</script>

<h1>Welcome to SvelteKit</h1>
<button on:click={increment}>{count}</button>

<style>
  button {
    width: 100px;
    height: 100px;
    background: mediumpurple;
    font-size: 2rem;
  }
</style>
