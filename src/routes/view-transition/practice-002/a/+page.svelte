<script>
	import { goto } from '$app/navigation';
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	const pageName = $page.url.pathname.split('/').at(-1);
	const viewTransitionName =	$page.url.pathname.split('/').at(-2);

	onMount(() => {
		console.log('onMount');
		const time = setTimeout(() => {goto('b')}, 1000);

		return () => {
			console.log('clearing timeout');
			clearTimeout(time);
		}
	})
</script>
<h2>
	pageName = {pageName}
</h2>
<div style="--view-transition-name:{viewTransitionName}" id={viewTransitionName}>
	a is for Apple <br>
	a is for Ant <br>
	a is for Alligator <br>
	a is for Airplane

	<div id="hi">
		hi
	</div>
</div>