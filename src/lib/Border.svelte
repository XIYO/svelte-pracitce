<script>
	const { viewTransitionName } = $props();
</script>
<h2>Border component</h2>

<div style="--view-transition-name: {viewTransitionName}">
		<slot />
</div>


<style>
		div {
				color: red;

				border: 10px solid;
				border-image: url('/octagon.svg') 33%;
		}
</style>