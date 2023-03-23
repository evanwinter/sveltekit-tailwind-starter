<script lang="ts">
	export let underline: boolean = true;
	const underlineClasses = underline ? 'underline underline-offset-8' : '';
</script>

<!-- svelte-ignore a11y-missing-attribute -->
<a
	{...$$restProps}
	class="{underlineClasses} text-gray-800 hover:text-gray-400 transition-colors {$$restProps.class}"
>
	<slot />
</a>
