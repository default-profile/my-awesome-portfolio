<script lang="ts">
	import SocialIcons from '$lib/assets/socials.svg';
</script>

<footer class="overflow-x-hidden py-18 xl:flex xl:items-start">
	<div class="xl:shrink-0 xl:grow xl:basis-0">
		<div class="xl:mr-48">
			<div class="mb-10 typography-headline">Let's work together</div>
			<div class="typography-body-sm">
				This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com This is a template Figma
				file, turned into code using Anima. Learn more at AnimaApp.com
			</div>
			<img src={SocialIcons} alt="Social Icons" class="mt-15" />
		</div>
	</div>
	<div class="mt-20 xl:mt-0 xl:shrink-0 xl:grow xl:basis-0">
		<form class="space-y-5">
			<input type="text" placeholder="Name" class="w-full bg-[#F3F3F3] px-8 py-5 typography-body-sm" />
			<input type="email" placeholder="Email" class="w-full bg-[#F3F3F3] px-8 py-5 typography-body-sm" />
			<textarea rows="10" placeholder="Type your message here" class="w-full bg-[#F3F3F3] px-8 py-5 typography-body-sm"
			></textarea>
			<button class="mt-10 bg-[#2D2D2D] px-20 py-6 typography-body-sm text-white">Submit</button>
		</form>
	</div>
</footer>
