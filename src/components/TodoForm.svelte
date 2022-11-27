<script>
	let todo = '';
	import { addTodo } from '../stores/todoStore';
	function handleSubmit() {
		addTodo(todo);
		// console.log('submitting');
	}
</script>

<form
	on:submit|preventDefault={handleSubmit}
	action=""
	class="sm:w-2/4 p-5 border rounded shadow-lg mt-5 mx-auto"
>
	<div>
		<label for="todo" class="font-semibold text-lg">Todo :</label>
		<input
			bind:value={todo}
			type="text"
			name="todo"
			id="todo"
			class="input"
			placeholder="Watcha gotta do?"
		/>
	</div>
	<div class="text-right">
		<button class="btn-indigo-sm rounded mt-2" type="submit">Submit</button>
	</div>
</form>
