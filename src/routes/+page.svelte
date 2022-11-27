<script>
	import TodoForm from '../components/TodoForm.svelte';
	import { todos } from '../stores/todoStore';
	import Todo from '../components/Todo.svelte';
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<div class="text-center">
	<h1 class="font-semibold text-2xl">ToDo's App</h1>
</div>
<TodoForm />

{#each $todos as todo}
	<!-- <div>{todo.text}</div> -->
	<Todo {todo} />
{/each}
