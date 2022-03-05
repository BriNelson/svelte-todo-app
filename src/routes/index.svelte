<script>
function handleClick() {

    console.log('the click listener is working')
  }
</script>

<form on:submit|preventDefault={handleClick}>
    <input type="text" value="task">
    <input type="text" value="category">
    <button>Add Task</button>
</form>

<ul>
  <li></li>
</ul>

<style>

</style>
