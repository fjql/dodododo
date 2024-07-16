<script>
  let todos = $state([
    { title: "1", text: "", done: false },
    { title: "2", text: "", done: false },
    { title: "3", text: "", done: false },
    { title: "4", text: "", done: false },
    { title: "5", text: "", done: false },
    { title: "6", text: "", done: false },
  ]);
</script>

<main>
  {#each todos as todo}
    <div class="todo">
      <header>
        <h2>{todo.title}</h2>
        <input type="checkbox" value={todo.done}/>
      </header>
      {#if todo.text}
        <p>{todo.text}</p>
      {/if}
    </div>
  {/each}
  <div class="addtodo">
    <div class="details">
      <input type="text" placeholder="Enter Title..."/>
      <input type="text" placeholder="Enter Text..."/>
    </div>
    <button>Add</button>
  </div>
</main>

<style>
  main {
    position: relative;
    left: 50%;
    translate: -50% 0%;

    height: 100%;
    width: 80dvw;
    padding: .5rem;

    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(10vmax, 30vmax));
    gap: .25rem;
    justify-content: center;
    align-items: stretch;
  }

  .todo {
    border: 2px solid rgb(19, 15, 15);
    padding: .5rem 1rem;

    header {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
    }
  }

  .addtodo {
    border: 2px solid rgb(19, 15, 15);
    padding: .5rem 1rem;

    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: .25rem;

    .details {
      display: flex;
      flex-direction: column;
      gap: .25rem;
    }
  }
</style>