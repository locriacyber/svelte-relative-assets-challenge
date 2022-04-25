<script>
	import { onMount } from 'svelte';
	
	let Thing;
	
	const sleep = ms => new Promise(f => setTimeout(f, ms));
	
	onMount(async () => {
		await sleep(1000); // simulate network delay
		Thing = (await import('../import-me.css')).default;
	})
</script>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
