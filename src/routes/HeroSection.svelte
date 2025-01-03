<script lang="ts">
	import HeroImage from '$lib/assets/hero.svg';
</script>

<header
	class="flex h-[calc(100svh-var(--navbar-height))] min-h-180 flex-col items-center justify-between pt-12 pb-15 md:h-auto md:min-h-auto md:flex-row md:py-25"
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
		class="aspect-auto grow self-stretch overflow-hidden md:-mr-13 md:ml-12 md:object-cover md:object-left xl:m-0 xl:object-contain xl:object-center"
	/>
</header>
