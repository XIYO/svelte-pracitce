<script>
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';

	onMount(() => {
		const time = setTimeout(() => {goto('a');}, 2000);

		return () => {
			console.log('cleanup');
			clearTimeout(time);
		};
	});
</script>
clear