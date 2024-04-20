<script>
	import { onNavigate } from '$app/navigation';

	onNavigate((navigation) => {
		if (!document.startViewTransition) return;

		return new Promise((resolve) => {
			const transition = document.startViewTransition(async () => {
				resolve();
				await navigation.complete;
			});

			// transition.updateCallbackDone.then(() => {
			// 	alert('updateCallbackDone');
			// });
			//
			// transition.ready.then((e) => {
			// 	console.log(e);
			// 	alert('ready');
			// });
			//
			// transition.finished.then(() => {
			// 	alert('finished');
			// });
		});
	});
</script>

<main>
	<slot />
</main>