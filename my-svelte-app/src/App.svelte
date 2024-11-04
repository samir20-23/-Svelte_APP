<script>
	let items = ["Learn Svelte", "Build a Svelte app"];
	let newItem = "";
  
	function addItem() {
	  if (newItem.trim()) {
		items = [...items, newItem];
		newItem = "";
	  }
	}
  </script>
  
  <main>
	<h1>My To-Do List</h1>
	<ul>
	  {#each items as item}
		<li>{item}</li>
	  {/each}
	</ul>
  
	<input 
	  type="text" 
	  bind:value={newItem} 
	  placeholder="Add a new item" 
	/>
	<button on:click={addItem}>Add Item</button>
  </main>
  
  <style>
	main {
	  text-align: center;
	  padding: 1rem;
	  font-family: Arial, sans-serif;
	}
  
	ul {
	  list-style: none;
	  padding: 0;
	}
  
	li {
	  margin: 0.5rem 0;
	}
  
	input, button {
	  padding: 0.5rem;
	  font-size: 1rem;
	}
  
	button {
	  margin-left: 0.5rem;
	}
  </style>
  