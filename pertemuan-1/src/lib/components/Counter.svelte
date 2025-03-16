<!-- state -->

<script>
  let total = $state({
    total: 0,
    anull: 0,
    bnull: 0,
  });

  // @ts-ignore
  function handleForm(e) {
    let form = new FormData(e.target);
    let a = Number(form.get("a"));
    let b = Number(form.get("b"));

    total.total = a + b;
  }
  //@ts-ignore
  function handleReset(e) {
    total.total = 0;
    total.anull = 0;
    total.bnull = 0;
  }
</script>

<form onsubmit={handleForm}>
  <input type="number" name="a" bind:value={total.anull} />
  <input type="number" name="b" bind:value={total.bnull} />
  <button>click</button>
</form>
<button onclick={handleReset}>Reset</button>
<h1>HASIL : {total.total}</h1>
