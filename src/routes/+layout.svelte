<script>
	import favicon from '$lib/assets/carter.png';
	import '../app.css';
	import { onMount } from "svelte";
	import NavBar from "$lib/NavBar.svelte";
	import Hero from "$lib/Hero.svelte";

	onMount(() => {
		const media = window.matchMedia("(prefers-color-scheme: dark)");

		media.addEventListener("change", (themeChange) => {
			document.documentElement.dataset.theme = themeChange.matches ? "mocha" : "latte";
		});
	});

	let { children } = $props();
</script>

<NavBar />

<Hero title="Carter Constantine"/>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}