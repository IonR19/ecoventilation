<script lang="ts">
	const quickLinks = [
		{ title: 'about ecoair', url: '/about' },
		{ title: 'products', url: '/products' },
		{ title: 'services', url: '/services' },
		{ title: 'career', url: '/career' },
		{ title: 'contact', url: '/contact' }
	];
</script>

<footer class="bg-slate-900 text-white">
	<div class="container mx-auto flex pt-10">
		<div class="flex flex-1 flex-col p-4">
			<h4 class="mb-4 text-xl font-bold uppercase">about ecoair ventillation</h4>
			<p class="mt-4">
				Eco Air Ventilation is dedicated to full and complete compliance with all laws and
				regulations relevant to the conduct of its business.
			</p>
			<a class="mt-4" href="tel:+971 55 750 5187">+971 55 750 5187</a>
			<a class="mt-2" href="tel:+971 56 327 4913">+971 56 327 4913</a>
			<a class="mt-2" href="tel:+971 65 390 059">+971 65 390 059</a>
		</div>
		<div class="flex flex-1 flex-col p-4 text-center">
			<h4 class="mb-4 text-xl font-bold uppercase">quick links</h4>
			<ul>
				{#each quickLinks as link}
					<li class="mt-2 capitalize"><a href={link.url}>{link.title}</a></li>
				{/each}
			</ul>
		</div>
		<div class="flex flex-1 flex-col">
			<h4 class="mb-4 p-4 text-center text-xl font-bold uppercase">working hours</h4>
			<p class="mt-2">Contact us to know if open on special occasions.</p>
			<p class="mt-2">Sat - Thur: 8:00AM - 6:00PM</p>
			<p class="mt-2">Friday: Closed</p>
		</div>
	</div>
	<div class="p-4">
		<p class="text-center font-bold uppercase">
			copyright &copy; 2022 <span class="cursor-default transition-colors hover:text-orange-700"
				>Ecoair Ventilations</span
			>
		</p>
	</div>
</footer>
