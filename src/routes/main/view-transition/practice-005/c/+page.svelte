<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';
	import Border from '$lib/Border.svelte';
	import BorderGrid from '$lib/BorderGrid.svelte';

	const pageName = $page.url.pathname.split('/').at(-1);
	const viewTransitionName = $page.url.pathname.split('/').at(-2);

	// onMount(() => {
	// 	const time = setTimeout(() => {goto('d');}, 2000);
	// 	return () => clearTimeout(time);
	// });
</script>
<h1>
	pageName = {pageName}
</h1>
<BorderGrid viewTransitionName={viewTransitionName} >
	c is for Cat <br>
	c is for Car <br>
	c is for Cow <br>
	c is for Camel <br>
	c is for Cheetah <br>
	c is for Cat <br>
	c is for Car <br>
	c is for Cow <br>
	c is for Camel <br>
	c is for Cheetah <br>
	c is for Cat <br>
	c is for Car <br>
	c is for Cow <br>
	c is for Camel <br>
	c is for Cheetah <br>
	c is for Cat <br>
	c is for Car <br>
	c is for Cow <br>
	c is for Camel <br>
	c is for Cheetah <br>
	c is for Cat <br>
	c is for Car <br>
	c is for Cow <br>
	c is for Camel <br>
	c is for Cheetah <br>
</BorderGrid>