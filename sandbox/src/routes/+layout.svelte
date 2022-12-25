<script lang="ts">
	import '../app.css';

	import Footer from '$lib/Footer.svelte';
	import Header from '$lib/Header.svelte';
</script>

<Header />

<main class="p-8 bg-gradient-to-br from-blue-100 to-blue-200 w-full">
	<slot />
</main>

<Footer />
