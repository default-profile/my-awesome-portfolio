<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

<div class="px-7 md:px-13 xl:px-25">
	{@render children()}
</div>
