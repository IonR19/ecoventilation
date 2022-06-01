<script>
	import '../app.css';
	import Footer from '../lib/components/Footer.svelte';
	import Navbar from '../lib/components/Navbar.svelte';

	import nProgress from 'nprogress';
	import { navigating } from '$app/stores';

	import 'nprogress/nprogress.css';

	nProgress.configure({
		minimum: 0.16,
	});

	$: {
		if ($navigating) {
			nProgress.start();
		}
		if (!$navigating) {
			nProgress.done();
		}
	}
</script>

<Navbar />
<slot />
<Footer />
