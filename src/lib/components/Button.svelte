<button
	{...$$restProps}
	class="text-sm bg-gray-200 px-2 py-1 rounded-md hover:text-white hover:bg-black active:scale-95 transition-all {$$restProps.class}"
>
	<slot />
</button>
