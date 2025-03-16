<script>
  let datas = $state([
    {
      title: "data",
    },
  ]);
  //@ts-ignore
  function handleInput(e) {
    const form = new FormData(e.target);
    let title = form.get("title");
    datas.push({
      // @ts-ignore
      title: title,
    });
  }
</script>

<form action="" onsubmit={handleInput}>
  <input type="text" name="title" />
  <button>submit</button>
</form>

<ul>
  {#each datas as d}
    <li>{d.title}</li>
  {/each}
</ul>
