<script>
	import HeroContent from "../components/HeroContent.svelte";
	import Shader from "../components/Shader.svelte";
</script>

<div>
	<section class="relative h-screen">
		<Shader />
		<HeroContent />
	</section>

	<section class="grid grid-cols-1 md:grid-cols-2 gap-8 p-8 md:p-16">
		<div
			class="bg-base-300 rounded-lg flex items-center justify-center aspect-square"
		>
			<span class="text-base-content/50 text-lg">Photo</span>
		</div>
		<div class="prose flex flex-col justify-center">
			<h2>About Me</h2>
			<p>
				I'm a fullstack software engineer with experience building
				customer-facing enterprise applications at scale. I've worked across the
				entire stack — from product features end users interact with daily, to
				the services that power them, to the platform infrastructure underneath.
				I care about writing software that ships reliably and scales to meet
				real business demands.
			</p>
			<p>
				Outside of work, I'm a husband, a father of one, a chess and reading
				enthusiast, and the outnumbered owner of a dog and two cats.
			</p>
		</div>
	</section>
</div>
