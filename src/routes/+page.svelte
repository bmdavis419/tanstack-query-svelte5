<script>
	import { createQuery } from '$lib/createQuery.js';

	const myFirstQuery = createQuery({
		queryFn: async () => {
			console.log('we in first query :0');
			return Math.random();
		},
		queryKey: ['first']
	});

	$inspect($myFirstQuery.data);
</script>

<h1>Welcome to your library project</h1>
<p>Create your package using @sveltejs/package and preview/showcase your work with SvelteKit</p>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>
