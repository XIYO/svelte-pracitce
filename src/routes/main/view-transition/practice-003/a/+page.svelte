<script>
	import { goto } from '$app/navigation';
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	const pageName = $page.url.pathname.split('/').at(-1);
	const viewTransitionName =	$page.url.pathname.split('/').at(-2);

	// onMount(() => {
	// 	const time = setTimeout(() => {goto('b');}, 2000);
	// 	return () => clearTimeout(time);
	// });
</script>
<h1>
	pageName = {pageName}
</h1>
<div id={viewTransitionName}>
	a is for Apple <br>
	a is for Ant <br>
	a is for Alligator <br>
	a is for Airplane
</div>