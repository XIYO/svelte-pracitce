<script>
	const { size, bgColor } = $props();
</script>

<div style='--size:{size}; --bg-color:{bgColor};'>
	<slot />
</div>

<style>
    div {
        width: calc(var(--size, 1) * 1rem);
        height: calc(var(--size, 1) * 1rem);
        background-color: var(--bg-color);
				padding: 2rem;

				/*border: 1rem solid deepskyblue;*/
				/*border-radius: 1rem;*/

        border-image: url('/octagon-red.svg') 33% / 30px;

				view-transition-name: box;
    }
</style>