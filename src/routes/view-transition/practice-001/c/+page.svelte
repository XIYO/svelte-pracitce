<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';

	const pageName = $page.url.pathname.split('/').at(-1);

	onMount(() => {
		setTimeout(() => {goto('a')}, 1000);
	})
</script>
<h2>
	pageName = {pageName}
</h2>
<div id="practice-001">
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

<style>
	div {
		border: 5px solid #181818;
		border-radius: 5px;
	}
</style>