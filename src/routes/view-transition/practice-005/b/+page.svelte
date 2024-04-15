<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';
	import Border from '$lib/Border.svelte';
	import BorderGrid from '$lib/BorderGrid.svelte';

	const pageName = $page.url.pathname.split('/').at(-1);
	const viewTransitionName =	$page.url.pathname.split('/').at(-2);

	// onMount(() => {
	// 	const time = setTimeout(() => {goto('c');}, 2000);
	// 	return () => clearTimeout(time);
	// });
</script>
<h1>
	pageName = {pageName}
</h1>
<BorderGrid viewTransitionName={viewTransitionName} >	b is for Banana <br>
	b is for Ball <br>
	b is for Bat <br>
	b is for Bear <br>
	b is for Bird
</BorderGrid>