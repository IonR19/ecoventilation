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
	<dir class="container mx-auto flex items-center justify-between m-0">
		<div class="flex-grow-1">
			<img
				src="//cdn.shopify.com/s/files/1/0025/0245/9450/files/logo_3_large.png?v=1587770302"
				alt="logo"
				class="w-28"
			/>
		</div>
		<div>
			<ul class="flex items-center">
				{#each urls as url}
					<li class="mx-2 px-2 uppercase transition-all hover:text-lg hover:text-yellow-600">
						<a href={url.url}>{url.name}</a>
					</li>
				{/each}
			</ul>
		</div>
	</dir>
</nav>
