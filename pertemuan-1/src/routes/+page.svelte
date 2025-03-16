<!-- <script>
  // code scope js/ts
  let count = $state(0); //string array object number boolean

  function handleCount() {
    count++;
  }

  const data = $state([
    {
      name: "zulple",
      kelas: 20,
    },
  ]);

  data.push({
    name: "hasss",
    kelas: 23,
  });

  let data2 = $state.raw({
    merek: "org",
    bount: 23,
  });

  data2 = {
    merek: "oke",
    bount: 43,
  };

  let counti = $state(1);
  let doubled = $derived(count * 2);
  $effect(() => {});
</script>


<button onclick={handleCount}>
  click {count}
</button>

<button onclick={() => counti++}>
  {doubled}
</button>

<p>{counti} doubled is {doubled}</p> -->

<!-- <script>
  let state = $state({ value: 0 });
  let derived = $derived({ value: state.value * 2 });

  // this will run once, because `state` is never reassigned (only mutated)
  $effect(() => {
    state;
  });

  // this will run whenever `state.value` changes...
  $effect(() => {
    state.value;
  });

  // ...and so will this, because `derived` is a new object each time
  $effect(() => {
    derived;
  });
</script>

<button onclick={() => (state.value += 1)}>
  {state.value}
</button>

<p>{state.value} doubled is {derived.value}</p> -->

<script module>
  import Counter from "$lib/components/Counter.svelte";
</script>

<Counter />
