<script>
	import Pump from '$lib/Pump.svelte';

	let size = $state(15);
	let burst = $state(false);

	function reset() {
		size = 15;
		burst = false;
	}
</script>

<Pump
	inflate={() => {
		console.log('inflate', size, burst);
		size += 5;
		if (size > 75) burst = true;
	}}
	deflate={() => {
		if (size > 0) size -= 5;
	}}
/>

{#if burst}
	<button onclick={reset}>new balloon</button>
	<span class="boom">💥</span>
{:else}
	<span class="balloon" style="scale: {0.1 * size}">
		🎈
	</span>
{/if}

<style>
	span {
			display: inline-block;
	}
</style>