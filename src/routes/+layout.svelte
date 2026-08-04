<script>
	import favicon from '$lib/assets/carter.png';
	import '../app.css';
	import { onMount } from "svelte";

	onMount(() => {
		const media = window.matchMedia("(prefers-color-scheme: dark)");

		media.addEventListener("change", (themeChange) => {
			document.documentElement.dataset.theme = themeChange.matches ? "mocha" : "latte";
		});
	});

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}