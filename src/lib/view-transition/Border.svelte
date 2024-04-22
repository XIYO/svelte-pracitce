<script>
	const { viewTransitionName } = $props();
</script>
<div
	style="--view-transition-name: border-wrapper;"
	class="border">
	<div
		style="--view-transition-name: content;"
	>
		<slot />
	</div>
</div>

<style>
    :root {
        --color-default-black: hsl(200, 4%, 16%);
        --color-default-white: hsl(42, 66%, 93%);
        --color-primary: hsl(176, 89%, 37%);
    }

    .border {
        --padding: 1rem;

        background-color: var(--color-default-white);
        border-color: var(--color-default-black);

        border-radius: calc(var(--padding) * 1.5);
        border-width: 0.5rem;
        border-style: solid;
        overflow: clip;

				/*view-transitino-name: border-wrapper;*/
    }
</style>