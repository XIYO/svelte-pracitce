<script>
	const { viewTransitionName } = $props();
</script>
<h2>Border component</h2>

<div style="--view-transition-name: {viewTransitionName}">
		<slot />
</div>


<style>
		div {
				color: blue;

				/*border: 10px solid yellowgreen;*/
				/*border-radius: 10px;*/
				/*border-image: url('/skull-border.svg') 32 fill / 32px / 32px round;*/
				/*border-image: url('/octagon.svg') 33% / 10px / 10px;*/
				/*border-size: 30px;*/
				/*border-style: solid;*/
				/*border-image-size: 20px;*/
				/*border-image-slice: 33%;*/

				/* 보더 속성 테스트 1*/
				/*border-image-source: url('/skull-border.svg');*/
				/*border-image-slice: 33%;*/
				/*border-image-size: 30px;*/

				/* 보더 속성 테스트 2, 단축 문법 */
        /*border-image: url('/skull-border.svg') 33% / 30px;*/
				border-style: solid;
				border-width: 30px;
				/*border-color: darkmagenta;*/
				border-color: transparent;

        /*border: 24px solid;*/
        /*border-image: url(/skull-border.svg) 32 / 32px / 30px round;*/
		}
</style>