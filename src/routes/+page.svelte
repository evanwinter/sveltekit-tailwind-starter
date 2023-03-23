<script lang="ts">
	import Blurb from '$lib/components/Blurb.svelte';
	import Button from '$lib/components/Button.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Link from '$lib/components/Link.svelte';
	import { Reveal } from '@evanwinter/svelte-reveal';

	const heroTimeline = {
		headline: 0,
		summary: 200,
		button1: 250,
		button2: 300,
		video: 700
	};

	const contentTimeline = {
		intro: 0,
		blurb1: 200,
		blurb2: 300
	};
</script>

<Hero {heroTimeline}>
	<svelte:fragment slot="headline">Culpa ex officia officia eu est.</svelte:fragment>
	<svelte:fragment slot="summary">
		Tempor qui proident quis eu. In fugiat mollit deserunt nisi cillum occaecat sit qui.
		Exercitation laboris anim non consectetur deserunt consequat incididunt adipisicing minim.
	</svelte:fragment>
	<svelte:fragment slot="buttons">
		<Reveal delay={heroTimeline.button1}>
			<Button>See the Product</Button>
		</Reveal>
		<Reveal delay={heroTimeline.button2}>
			<Button>Book a Demo</Button>
		</Reveal>
	</svelte:fragment>
</Hero>

<div class="m-8 grid lg:grid-cols-2 gap-8">
	<Reveal delay={contentTimeline.intro}>
		<p class="text-2xl lg:max-w-2xl">
			Est sunt occaecat amet fugiat consequat enim. Aute velit exercitation cillum officia nostrud
			non cillum dolor ut quis non enim. Esse laborum laboris fugiat qui cupidatat ipsum dolore
			dolore fugiat reprehenderit consequat do. Sunt eu dolor sint qui eu Lorem Lorem consectetur
			amet nulla officia ad adipisicing cillum. Incididunt veniam ullamco ullamco fugiat sint ea
			consequat sit proident Lorem.
		</p>
	</Reveal>
	<div class="grid sm:grid-cols-2 sm:mt-6 lg:mt-0 lg:grid-cols-1 gap-8 lg:gap-12">
		<Reveal delay={contentTimeline.blurb1}>
			<Blurb>
				<svelte:fragment slot="pill">Lorem Ipsum</svelte:fragment>
				<svelte:fragment slot="text">
					Deserunt magna do nostrud laboris est est. Cillum irure do amet ea fugiat. Voluptate ipsum
					aute ad veniam. Duis tempor aute velit proident exercitation incididunt culpa cupidatat
					officia ad eu. Ut id officia non minim fugiat. Culpa amet cillum non id et elit sint.
					Nulla deserunt consequat dolor ut laborum mollit.
				</svelte:fragment>
				<svelte:fragment slot="links">
					<Link href="/">Tempor voluptate</Link>
					<Link href="/">Enim ullamco</Link>
				</svelte:fragment>
			</Blurb>
		</Reveal>

		<Reveal delay={contentTimeline.blurb2}>
			<Blurb>
				<svelte:fragment slot="pill">Dolor siti</svelte:fragment>
				<svelte:fragment slot="text">
					Est Lorem nulla veniam eu. Proident duis velit laboris consectetur ullamco excepteur non
					fugiat ipsum amet. Ad anim ex aliqua adipisicing aliqua duis ea cillum. Velit ipsum aute
					et consequat incididunt amet fugiat nisi ex. Nulla quis ullamco exercitation anim sunt
					dolor cillum esse aute Lorem dolor minim proident est. Nisi nisi ut Lorem aute magna ipsum
					laborum ea voluptate incididunt.
				</svelte:fragment>
				<svelte:fragment slot="links">
					<Link href="/">Fugiat ea elit</Link>
				</svelte:fragment>
			</Blurb>
		</Reveal>
	</div>
</div>
