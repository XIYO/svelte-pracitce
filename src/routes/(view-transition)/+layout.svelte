<script>
	import './style.css';
	import { onNavigate } from '$app/navigation';

	onNavigate((navigation) => {
		if (!document.startViewTransition) return;

		return new Promise((resolve) => {
			// const borderBefore = document.querySelector('[style*="--view-transition-name: border"]');
			// console.log(borderBefore.firstChild.textContent);

			let borderAfter;

			const transition = document.startViewTransition(async () => {
				resolve();
				await navigation.complete;
			});

			transition.updateCallbackDone.then(() => {
				// alert('updateCallbackDone');
				// const borderAfter = document.querySelector('[style*="--view-transition-name: border"]');
				// console.log(borderAfter.firstChild.textContent);
			});

			transition.ready.then(() => {
				// alert('ready');
				borderAfter = document.querySelector('[style*="--view-transition-name: content"]');
				console.log(borderAfter.parentElement.style.backgroundColor);
				// borderAfter.parentElement.style.backgroundColor = 'transparent';
				// borderAfter.parentElement.style.borderColor = 'transparent';
			});

			transition.finished.then(() => {
				// alert('finished');
				// 백그라운드 컬러 스타일을 삭제하고싶어
				// borderAfter.parentElement.style.removeProperty('background-color');
				// borderAfter.parentElement.style.removeProperty('border-color');
			});
		});
	});
</script>

<main>
	<slot />
</main>