<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';

	const pageName = $page.url.pathname.split('/').at(-1);

	onMount(() => {
		console.log('onMount');
		const time = setTimeout(() => {goto('c')}, 1000);

		return () => {
			console.log('clearing timeout');
			clearTimeout(time);
		}
	})
</script>
<h2>
	pageName = {pageName}
</h2>
<div id="practice-001">
	b is for Banana <br>
	b is for Ball <br>
	b is for Bat <br>
	b is for Bear <br>
	b is for Bird
</div>