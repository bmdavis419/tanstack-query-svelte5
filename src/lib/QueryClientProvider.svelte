<script lang="ts">
	import { type Snippet } from 'svelte';
	import { QueryClient } from '@tanstack/query-core';
	import { setQueryClientContext } from './context.js';

	const {
		children,
		client = new QueryClient()
	}: {
		children: Snippet<[]>;
		client?: QueryClient;
	} = $props();

	$effect(() => {
		client.mount();

		return () => {
			client.unmount();
		};
	});

	setQueryClientContext(client);
</script>

{@render children()}
