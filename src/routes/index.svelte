<script>

  let newTodo = ''
  let todoList=[
    {todo: "work" , competed: false},
    {todo: "play" , competed: false},
    {todo: "run" , competed: false},
  ]
function handleClick() {
todoList = [...todoList, {todo: newTodo, competed: false}]
    console.log(todoList)
    console.log('the click listener is working')
    newTodo = ''
  }
  function removeTodo(index) {
    todoList.splice(index, 1)
    todoList = todoList
  }
</script>
<div class="container">
<form on:submit|preventDefault={handleClick}>
  <div class="row">
    <div class="col">
    <input class="form-control" type="text" bind:value={newTodo}>
    </div>
    <div class = "col">

    <button class="btn btn-primary" >Add Task</button>
  </div>

</div>
</form>


{#each todoList as item, index}

  <div class="">
  {item.todo}<button type="button" class="btn btn-danger" on:click={()=>removeTodo(index)} >delete</button>
  </div>
{/each}
</div>

<style>


</style>
