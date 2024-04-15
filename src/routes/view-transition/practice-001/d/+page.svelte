<script>
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';

	onMount(() => {
		console.log('onMount');
		const time = setTimeout(() => {goto('a')}, 1000);

		return () => {
			console.log('clearing timeout');
			clearTimeout(time);
		}
	})
</script>
clear