<script lang="ts">
	import Image4 from '$lib/assets/products/american-girl.svg';
	import Image1 from '$lib/assets/products/free-bird.svg';
	import Image2 from '$lib/assets/products/purple-haze.svg';
	import Image6 from '$lib/assets/products/under-pressure.svg';
	import Image5 from '$lib/assets/products/whole-lotta-love.svg';
	import Image3 from '$lib/assets/products/you-really-got-mee.svg';

	const x: Array<{ image: string; title: string; subtitle: string }> = [
		{ image: Image1, title: 'Free Bird', subtitle: 'Lynyrd Skynyrd' },
		{ image: Image2, title: 'Purple Haze', subtitle: 'Jimi Hendrix' },
		{ image: Image3, title: 'You Really Got Me', subtitle: 'The Kinks' },
		{ image: Image4, title: 'American Girl', subtitle: 'Tom Petty' },
		{ image: Image5, title: 'Whole Lotta Love', subtitle: 'Led Zeppelin' },
		{ image: Image6, title: 'Under Pressure ', subtitle: 'Queen' },
	];
</script>

<section class="pt-15 pb-23 md:pt-25 md:pb-38">
	<div class="mb-15 text-center typography-headline">Latest Work</div>
	<div class="grid grid-cols-1 justify-center gap-15 md:grid-cols-2 md:gap-12 xl:grid-cols-3 xl:gap-15">
		{#each x as { image, title, subtitle }}
			<div>
				<img src={image} alt={title} class="w-full" />
				<div class="mt-6 mb-2 typography-body-lg">{title}</div>
				<div class="typography-body-sm">{subtitle}</div>
			</div>
		{/each}
	</div>
</section>
