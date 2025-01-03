<script lang="ts">
	import ArtDirectionImage from '$lib/assets/services/art-direction.svg';
	import ProductDesignImage from '$lib/assets/services/product-design.svg';
	import VisualDesignImage from '$lib/assets/services/visual-deign.svg';

	const products: Array<{ image: string; title: string; description: string }> = [
		{
			image: ProductDesignImage,
			title: 'Product design',
			description: 'This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com',
		},
		{
			image: ArtDirectionImage,
			title: 'Art Direction',
			description: 'This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com',
		},
		{
			image: VisualDesignImage,
			title: 'Visual Design',
			description: 'This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com',
		},
	];
</script>

<section class="grid grid-cols-1 justify-items-center gap-32 py-38 md:grid-cols-2 md:py-45 xl:grid-cols-3">
	{#each products as { image, title, description }}
		<div class="flex w-62 flex-col items-center justify-center text-center">
			<img src={image} alt={title} class="size-32" />
			<div class="mt-14 mb-10 typography-title">{title}</div>
			<div class="typography-body-sm">{description}</div>
		</div>
	{/each}
</section>
