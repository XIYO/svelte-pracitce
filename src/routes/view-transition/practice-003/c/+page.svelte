<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';

	const pageName = $page.url.pathname.split('/').at(-1);
	const viewTransitionName = $page.url.pathname.split('/').at(-2);

	// onMount(() => {
	// 	setTimeout(() => {goto('d');}, 3000);
	// });
</script>
<h1>
	pageName = {pageName}
</h1>
<div id={viewTransitionName}>
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
</div>