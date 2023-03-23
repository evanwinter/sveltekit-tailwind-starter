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
	<Link underline={false} class="text-xl p-8 tracking-wide" href="/">BRAND</Link>

	<div
		bind:this={nav}
		class="fixed bg-white top-4 right-4 flex gap-4 p-4 rounded-lg border border-transparent z-10 transition-all"
	>
		<Link underline={false} href="/">Product</Link>
		<Link underline={false} href="/">Book a Demo</Link>
		<Link underline={false} href="/">About</Link>
		<Link underline={false} href="/">Mission</Link>
	</div>
</nav>
