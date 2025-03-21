<script lang="ts">
	import '../app.css';
	import Shell from '$lib/components/Shell.svelte';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';

	const menuItems: { href: string; text: string }[] = [
		{ href: '/', text: 'Home' },
		{ href: '/reasons', text: 'History' }
	];
</script>

<svelte:head>
	<script
		defer
		data-website-id="dcbd86f7-f89b-4bab-a089-362a08423860"
		src="https://umami.jonasclaes.be/script.js"
	></script>
</svelte:head>

<div>
	<Shell {menuItems}>
		<Header />

		<main>
			<slot />
		</main>

		<Footer />
	</Shell>
</div>
