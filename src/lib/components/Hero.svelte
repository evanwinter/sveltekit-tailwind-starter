<script lang="ts">
	import { Reveal } from '@evanwinter/svelte-reveal';
	export let heroTimeline: { [key: string]: number };
</script>

<div class="flex flex-col gap-8 lg:flex-row justify-between mx-8 mb-8 mt-16 md:mt-32">
	<Reveal direction="up" delay={heroTimeline.headline}>
		<h1 class="text-5xl md:text-7xl md:max-w-lg">
			<slot name="headline" />
		</h1>
	</Reveal>

	<div class="flex flex-col justify-between gap-4 lg:items-end">
		<Reveal delay={heroTimeline.summary}>
			<p class="lg:max-w-md">
				<slot name="summary" />
			</p>
		</Reveal>

		<div class="flex gap-4">
			<slot name="buttons" />
		</div>
	</div>
</div>

<Reveal delay={heroTimeline.video}>
	<div class="overflow-hidden rounded-3xl mx-8 aspect-video bg-white">
		<video preload="metadata" muted loop autoplay playsinline class="h-full object-cover">
			<source
				src="https://player.vimeo.com/progressive_redirect/playback/720723904/rendition/1080p/file.mp4?loc=external&amp;signature=051806af5169661efeed8177b4f3101699d88447a2356ba789017010b925c030"
				type="video/mp4"
			/>
		</video>
	</div>
</Reveal>
