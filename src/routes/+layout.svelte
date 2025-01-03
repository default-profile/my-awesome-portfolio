<script lang="ts">
	import '../app.css';
	import Footer from '$lib/Footer.svelte';
	import Navbar from '$lib/Navbar.svelte';
	let { children } = $props();
</script>

<div class="px-7 md:px-13 xl:px-25">
	<Navbar />
	{@render children()}
	<Footer />
</div>
