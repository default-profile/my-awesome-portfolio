<script lang="ts">
	import Footer from '$lib/Footer.svelte';
	import Navbar from '$lib/Navbar.svelte';
	import HeroImage from '$lib/assets/hero.svg';
	import ProductDesignImage from '$lib/assets/services/product-design.svg';
	import ArtDirectionImage from '$lib/assets/services/art-direction.svg';
	import VisualDesignImage from '$lib/assets/services/visual-deign.svg';
	import Image1 from '$lib/assets/products/free-bird.svg';
	import Image2 from '$lib/assets/products/purple-haze.svg';
	import Image3 from '$lib/assets/products/you-really-got-mee.svg';
	import Image4 from '$lib/assets/products/american-girl.svg';
	import Image5 from '$lib/assets/products/whole-lotta-love.svg';
	import Image6 from '$lib/assets/products/under-pressure.svg';
	import ProfilePicture1 from '$lib/assets/profiles/author-1.svg';
	import ProfilePicture2 from '$lib/assets/profiles/author-2.svg';
	import ProfilePicture3 from '$lib/assets/profiles/author-3.svg';
	import Rating from '$lib/assets/rating.svg';
	import { Apple, Awwards, Behance, Dribble, Google } from '$lib/assets/logos';

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

	const x: Array<{ image: string; title: string; subtitle: string }> = [
		{ image: Image1, title: 'Free Bird', subtitle: 'Lynyrd Skynyrd' },
		{ image: Image2, title: 'Purple Haze', subtitle: 'Jimi Hendrix' },
		{ image: Image3, title: 'You Really Got Me', subtitle: 'The Kinks' },
		{ image: Image4, title: 'American Girl', subtitle: 'Tom Petty' },
		{ image: Image5, title: 'Whole Lotta Love', subtitle: 'Led Zeppelin' },
		{ image: Image6, title: 'Under Pressure ', subtitle: 'Queen' },
	];

	const testimonies: Array<{ review: string; author: { profilePicture: string; name: string; company: string } }> = [
		{
			author: { profilePicture: ProfilePicture1, name: 'Gemma Nolen', company: 'Google' },
			review: 'This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com',
		},
		{
			author: { profilePicture: ProfilePicture2, name: 'Gemma Nolen', company: 'Google' },
			review: 'This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com',
		},
		{
			author: { profilePicture: ProfilePicture3, name: 'Gemma Nolen', company: 'Google' },
			review: 'This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com',
		},
	];
</script>

<Navbar />

<!-- Hero Section -->
<header
	class="flex h-[calc(100svh-var(--navbar-height))] min-h-auto flex-col items-center justify-between pt-12 pb-15 md:h-auto md:flex-row md:py-25"
>
	<div class="flex grow flex-col items-center text-center md:my-12 md:items-start md:text-start">
		<div class="typography-body-lg text-nowrap">Branding | Image making</div>
		<div class="mt-6 mb-5 typography-display text-nowrap md:my-10">
			My Awesome <br /> Portfolio
		</div>
		<div class="typography-body-sm">
			This is a template Figma file, turned into code using Anima. <br class="hidden xl:block" /> Learn more at AnimaApp.com
		</div>
	</div>
	<img
		src={HeroImage}
		alt="Hero"
		class="aspect-auto grow self-stretch md:-mr-13 md:ml-12 md:object-cover md:object-left xl:m-0 xl:object-contain xl:object-center"
	/>
</header>

<!-- Companies Marquee (Mobile) -->
<div class="flex items-center justify-center md:hidden">
	<div class="w-60 space-y-15 border-y-2 border-y-[rgba(0,0,0,0.2)] py-15">
		<div class="flex flex-row justify-between">
			<img src={Google} alt="Google" />
			<img src={Behance} alt="Behance" />
		</div>
		<div class="flex flex-row justify-between">
			<img src={Dribble} alt="Dribble" />
			<img src={Apple} alt="Apple" />
		</div>
		<img src={Awwards} alt="Awards" />
	</div>
</div>

<!-- Companies Marquee (Tablet, Desktop) -->
<div
	class="-mx-13 hidden flex-row items-center gap-x-33 overflow-x-hidden border-y-2 border-y-[rgba(0,0,0,.2)] px-13 py-17 md:flex xl:-mx-25 xl:px-25"
>
	<img src={Google} alt="Google" />
	<img src={Apple} alt="Apple" />
	<img src={Dribble} alt="Dribble" />
	<img src={Awwards} alt="Awards" />
	<img src={Behance} alt="Behance" />
</div>

<!-- Products Section -->
<section class="grid grid-cols-1 justify-items-center gap-32 py-38 md:grid-cols-2 md:py-45 xl:grid-cols-3">
	{#each products as { image, title, description }}
		<div class="flex w-62 flex-col items-center justify-center text-center">
			<img src={image} alt={title} class="size-32" />
			<div class="mt-14 mb-10 typography-title">{title}</div>
			<div class="typography-body-sm">{description}</div>
		</div>
	{/each}
</section>

<!-- Latest Work Section -->
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

<!-- Testimonies Section -->
<section class="border-b-2 border-b-[rgba(0,0,0,.2)] pt-15 pb-22">
	<div class="mb-10 text-center typography-headline">Clients</div>
	<div class="grid grid-cols-1 gap-15 md:grid-cols-2 xl:grid-cols-3">
		{#each testimonies as { author, review }}
			<div class="space-y-20 border-2 border-[#FFD285] bg-[#FFFCF5] p-8">
				<div class="typography-body-lg">{review}</div>
				<div class="flex items-start">
					<img src={author.profilePicture} alt={author.name} />
					<div class="ml-5 space-y-2 typography-body-sm">
						<img src={Rating} alt="Rating" />
						<div>{author.name}, <br /> {author.company}</div>
					</div>
				</div>
			</div>
		{/each}
	</div>
</section>

<Footer />
