<script>
	import Pill from '$lib/components/Pill.svelte';
</script>

<div class="flex flex-col gap-4 items-start lg:flex-row lg:gap-8">
	<Pill>
		<slot name="pill" />
	</Pill>

	<div>
		<p class="max-w-xl text-xl">
			<slot name="text" />
		</p>
		<div class="mt-6 flex gap-4">
			<slot name="links" />
		</div>
	</div>
</div>
