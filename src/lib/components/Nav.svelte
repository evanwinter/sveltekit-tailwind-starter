<script lang="ts">
	import Link from '$lib/components/Link.svelte';

	let nav: HTMLElement;
	const scrolledStyle: string[] = ['shadow-sm', 'border-gray-100'];
</script>

<svelte:window
	on:scroll={() => {
		if (window.scrollY > 0) {
			nav.classList.add(...scrolledStyle);
		} else {
			nav.classList.remove(...scrolledStyle);
		}
	}}
/>

<nav class="flex justify-between">
	<Link class="text-xl p-8" href="/">brand</Link>

	<div
		bind:this={nav}
		class="fixed bg-white top-4 right-4 flex gap-4 p-4 rounded-lg border border-transparent z-10 transition-all"
	>
		<Link href="/">Product</Link>
		<Link href="/">Book a Demo</Link>
		<Link href="/">About</Link>
		<Link href="/">Mission</Link>
	</div>
</nav>
