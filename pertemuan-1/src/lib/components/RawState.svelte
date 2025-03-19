<script lang="ts">
  type peopleType = {
    name: string;
    age: number;
  };

  let people = $state.raw<peopleType>({
    name: "angga",
    age: 40,
  });

  function hello() {
    people = {
      name: (document.getElementById("name") as HTMLInputElement).value,
      age: parseInt((document.getElementById("age") as HTMLInputElement).value),
    };
  }
</script>

<input type="text" id="name" />
<input type="number" id="age" />

<button onclick={hello}>click</button>

<h1>hello {people.name} kamu umur segini ya {people.age}</h1>
