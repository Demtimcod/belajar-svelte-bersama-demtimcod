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
  import DerivedBy from "$lib/components/DerivedBy.svelte";
  import DrevidedRunes from "$lib/components/DrevidedRunes.svelte";
  import EXampleGlobalState from "$lib/components/EXampleGlobalState.svelte";
  import GlobalState from "$lib/components/GlobalState.svelte";
  import RawState from "$lib/components/RawState.svelte";
  import TodoList from "$lib/components/TodoList.svelte";

  let count = $state(0);

  function handleCount() {
    count++;
  }
  // jika mau melihat perubahan menggunakn inspect
  //$inspect(count).with((type, values) => console.log(type, values));
</script>

<button onclick={handleCount}>test inspect</button>

<TodoList />

<RawState />

<DrevidedRunes />

<DerivedBy />

<GlobalState />

<EXampleGlobalState />

<a href="/effect" target="_blank">Menuju example effect</a>
