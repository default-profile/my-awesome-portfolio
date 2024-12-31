<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

<div class="px-7 md:px-13">
	{@render children()}
</div>
