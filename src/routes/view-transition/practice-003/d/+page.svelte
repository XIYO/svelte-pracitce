<script>
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';

	onMount(() => {
		setTimeout(() => {goto('a');}, 3000);
	});
</script>
clear