<script lang="ts">
	import type { Snippet } from 'svelte';
	import { useHydrate } from './useHydrate.js';
	import type { DehydratedState, HydrateOptions, QueryClient } from '@tanstack/query-core';

	const {
		state,
		options,
		queryClient,
		children
	}: {
		state: DehydratedState;
		options: HydrateOptions | undefined;
		queryClient: QueryClient | undefined;
		children: Snippet<[]>;
	} = $props();

	useHydrate(state, options, queryClient);
</script>

{@render children()}
