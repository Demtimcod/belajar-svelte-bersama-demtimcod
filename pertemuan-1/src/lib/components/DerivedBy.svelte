<script>
  let count = $state(0);
  let check = $derived.by(() => {
    if (count == 5) {
      return "Udah nyampek lima aja";
    } else {
      return "LOSSSSS";
    }
  });
</script>

<h1>Contoh derived.by</h1>

<h1>count: {count} status {check}</h1>

<button onclick={() => count++}>incremmet</button>
