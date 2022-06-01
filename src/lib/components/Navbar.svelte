<script lang="ts">
	const urls = [
		{ name: 'home', url: '/' },
		{ name: 'about', url: '/about' },
		{ name: 'products', url: '/products' },
		{ name: 'services', url: '/services' },
		{ name: 'career', url: '/career' },
		{ name: 'contact', url: '/contact' }
	];
</script>

<nav class="shadow-lg">
	<div class="mx-auto flex items-center justify-between px-10">
		<div>
			<a class="cursor-pointer" href="/">
				<img
					src="//cdn.shopify.com/s/files/1/0025/0245/9450/files/logo_3_large.png?v=1587770302"
					alt="logo"
					class="w-32"
				/>
			</a>
		</div>
		<ul class="flex h-20">
			{#each urls as url}
				<li
					class="flex items-center px-4 font-medium uppercase shadow-inner shadow-gray-300 transition-all hover:text-lg hover:text-yellow-600"
				>
					<a class=" text-xl" href={url.url}>{url.name}</a>
				</li>
			{/each}
		</ul>
	</div>
</nav>
