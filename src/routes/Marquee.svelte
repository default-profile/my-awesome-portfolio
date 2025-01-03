<script lang="ts">
	import { Apple, Awwards, Behance, Dribble, Google } from '$lib/assets/logos';
</script>

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
