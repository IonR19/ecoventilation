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
				src="https://ecoairventilation.com/wp-content/uploads/2021/09/logo-animated-ecoair-0.png"
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
