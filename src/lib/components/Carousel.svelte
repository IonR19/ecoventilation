<script lang="ts">
	function generateInterval() {
		return setInterval(() => {
			active = (active + 1) % urls.length;
		}, 3000);
	}

	let urls = [
		'https://images.unsplash.com/photo-1652663496063-88f77cca9ae1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80',
		'https://images.unsplash.com/photo-1652660521827-17394230d316?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
		'https://images.unsplash.com/photo-1651927110248-9f1f4b5803e2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=627&q=80',
		'https://images.unsplash.com/photo-1652653001146-25e6ac2d88d2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
		'https://images.unsplash.com/photo-1652664767434-9cf9447d499a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80'
	];

	let active = 0;

	let intervalV = generateInterval();

	function handleClick(i: number) {
		console.log(i);

		clearInterval(intervalV);
		active = i;
		intervalV = generateInterval();
	}
</script>

<div class="relative flex h-96 overflow-hidden border-4 border-gray-300">
	{#each urls as imageUrl}
		<div
			class="w-full shrink-0 basis-full transition-transform duration-1000"
			style={`transform: translateX(${-100 * active}%);`}
		>
			<img src={imageUrl} alt="wallpaper" class="h-full w-full object-cover" />
		</div>
		<div class="absolute bottom-5 left-1/2 flex -translate-x-1/2 justify-self-end">
			{#each urls as _, i (_)}
				<button
					class="bottom-2 left-4 mx-2 h-4 w-4 rounded-full border border-slate-200 bg-slate-700 transition-transform"
					class:scale-150={active == i}
					on:click={() => handleClick(i)}
				/>
			{/each}
		</div>
	{/each}
</div>
