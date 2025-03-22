<script>
  import { counter } from "$lib/global-state/counter.svelte";
</script>

<h1>Ini Example Global state</h1>
<button onclick={() => counter.count++}
  >tombol ini telah ditekan sekitar {counter.count}</button
>
