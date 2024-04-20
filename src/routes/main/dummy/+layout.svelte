<script>
	// import { url } from '$app/stores';
	import { onNavigate } from '$app/navigation';
	import Sample001 from '$lib/view-transition-samples/Sample001.svelte';

	onNavigate((navigation) => {
		if (!document.startViewTransition) return;

		return new Promise((resolve) => {
			document.startViewTransition(async () => {
				resolve();
				await navigation.complete;
			});
		});
	});
</script>
<div id="test">
	<!--{url.pathname}-->
</div>
<slot />

<!--<style>-->
<!--	:global(#content) {-->
<!--			background-color: cornflowerblue;-->
<!--			display: inline-block;-->
<!--			border: 1px solid black;-->

<!--			view-transition-name: full-embed;-->
<!--	}-->

<!--  :root::view-transition-old(full-embed),-->
<!--  :root::view-transition-new(full-embed) {-->
<!--      /* Prevent the default animation,-->
<!--			so both views remain opacity:1 throughout the transition */-->
<!--      /*animation: none;*/-->
<!--      /* Use normal blending,-->
<!--			so the new view sits on top and obscures the old view */-->
<!--      /*mix-blend-mode: normal;*/-->
<!--      /* Make the height the same as the group,-->
<!--			meaning the view size might not match its aspect-ratio. */-->
<!--      height: 100%;-->
<!--      /* Clip any overflow of the view */-->
<!--      /*overflow: clip;*/-->
<!--  }-->

<!--  /* The old view is the thumbnail */-->
<!--  :root::view-transition-old(full-embed) {-->
<!--      /* Maintain the aspect ratio of the view,-->
<!--			by shrinking it to fit within the bounds of the element */-->
<!--      object-fit: contain;-->
<!--      /*animation: 0.25s linear both shrink-x;*/-->
<!--  }-->

<!--  /* The new view is the full image */-->
<!--  :root::view-transition-new(full-embed) {-->
<!--      /* Maintain the aspect ratio of the view,-->
<!--			by growing it to cover the bounds of the element */-->
<!--      object-fit: cover;-->
<!--      /*animation: 0.25s 0.25s linear both grow-x;*/-->
<!--  }-->

<!--  @keyframes grow-x {-->
<!--      from {-->
<!--          transform: scaleX(0);-->
<!--      }-->
<!--      to {-->
<!--          transform: scaleX(1);-->
<!--      }-->
<!--  }-->

<!--  @keyframes shrink-x {-->
<!--      from {-->
<!--          transform: scaleX(1);-->
<!--      }-->
<!--      to {-->
<!--          transform: scaleX(0);-->
<!--      }-->
<!--  }-->
<!--</style>-->