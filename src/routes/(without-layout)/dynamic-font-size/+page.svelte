<script>
	import DynamicFontSizeEm from '$lib/DynamicFontSize/DynamicFontSizeEm.svelte';
	import DynamicFontSizeRem from '$lib/DynamicFontSize/DynamicFontSizeRem.svelte';
</script>

<div class="container">
	<div id="double-rem">
		<div class="sub-title">
			폰트 사이즈는 2rem입니다.
		</div>
		<DynamicFontSizeEm>DOUBLE-EM</DynamicFontSizeEm>
		<DynamicFontSizeRem>DOUBLE-REM</DynamicFontSizeRem>
	</div>
	<div id="half-rem">
		<div class="sub-title">
			폰트 사이즈는 0.5rem입니다.
		</div>
		<DynamicFontSizeEm>HALF-EM</DynamicFontSizeEm>
		<DynamicFontSizeRem>HALF-REM</DynamicFontSizeRem>
	</div>
</div>

<style>
    .sub-title {
        padding: 1rem;
        font-size: 1rem;
    }

    #double-rem {
        font-size: 2rem;

        background-color: palegreen;
        border-radius: 2rem;
    }

    #half-rem {
        font-size: 0.5rem;

        background-color: salmon;
        border-radius: 0.5rem;
    }
</style>