<script lang="ts" context="module">
	import type { Load } from '@sveltejs/kit';

	export const load: Load = async (p) => {
		return {
			props: {
				errorCode: p.status
			}
		};
	};
</script>

<script lang="ts">
	export let errorCode: number;
</script>

<h1 class="my-10 text-center text-6xl font-bold uppercase text-red-600">Error {errorCode}</h1>
<p class="text-center text-4xl capitalize text-red-600">Try again later</p>
<blockquote>
	<p>Not Found</p>
</blockquote>
