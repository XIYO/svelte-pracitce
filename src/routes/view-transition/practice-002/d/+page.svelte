<script>
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';

	onMount(() => {
		setTimeout(() => {
			goto('a');
		}, 1000);
	});
</script>
clear