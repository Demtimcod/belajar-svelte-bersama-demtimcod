<script>
  import { counter } from "$lib/hooks/counter.svelte";

  function handeleGlobalCounter() {
    counter.count++;
  }
</script>

<h1>Global State</h1>

<button onclick={handeleGlobalCounter}>counter : {counter.count}</button>
