<script lang="ts">
	import Rating from '$lib/assets/rating.svg';
	import ProfilePicture1 from '$lib/assets/profiles/author-1.svg';
	import ProfilePicture2 from '$lib/assets/profiles/author-2.svg';
	import ProfilePicture3 from '$lib/assets/profiles/author-3.svg';

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
