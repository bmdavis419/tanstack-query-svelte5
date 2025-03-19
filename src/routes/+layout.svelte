<script>
	import QueryClientProvider from '$lib/QueryClientProvider.svelte';

	const { children } = $props();
</script>

<QueryClientProvider>
	{@render children()}
</QueryClientProvider>
