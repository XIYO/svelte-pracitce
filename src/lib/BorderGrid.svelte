<script>
	const { viewTransitionName } = $props();
</script>
<h2>Border-Grid component</h2>

<!--<div style="&#45;&#45;view-transition-name: {viewTransitionName}">-->
<div>
	<span style="--view-transition-name: top-left-{viewTransitionName}" class='top-left'></span>
	<span style="--view-transition-name: top-edge-{viewTransitionName}" class="top-edge"></span>
	<span style="--view-transition-name: top-right-{viewTransitionName}" class="top-right"></span>
	<span style="--view-transition-name: left-edge-{viewTransitionName}" class="left-edge"></span>
	<span style="--view-transition-name: {viewTransitionName}"><slot /></span>
	<span style="--view-transition-name: right-edge-{viewTransitionName}" class="right-edge"></span>
	<span style="--view-transition-name: bottom-left-{viewTransitionName}" class="bottom-left"></span>
	<span style="--view-transition-name: bottom-edge-{viewTransitionName}" class="bottom-edge"></span>
	<span style="--view-transition-name: bottom-right-{viewTransitionName}" class="bottom-right"></span>
</div>

<style>
    div {
        color: cornflowerblue;

        /*border: 10px solid;*/
        /*border-image: url('/octagon.svg') 33%;*/

				display: grid;
				grid-template-columns: auto 1fr auto;
    }

		span {
				border-width: 0;
				border-style: solid;
        border-image: url('/test.png') 33%;
		}

		.top-left {
				border-inline-start-width: 10px;
				border-block-start-width: 10px;
		}

		.top-edge {
				border-block-start-width: 10px;
		}

		.top-right {
				border-inline-end-width: 10px;
				border-block-start-width: 10px;
		}

		.left-edge {
				border-inline-start-width: 10px;
		}

		.right-edge {
				border-inline-end-width: 10px;
		}

		.bottom-left {
				border-inline-start-width: 10px;
				border-block-end-width: 10px;
		}

		.bottom-edge {
				border-block-end-width: 10px;
		}

		.bottom-right {
				border-inline-end-width: 10px;
				border-block-end-width: 10px;
		}
</style>