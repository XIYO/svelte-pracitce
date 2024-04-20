<div class="rem">
	<h2>
		Dynamic Font Size - <slot />
	</h2>
	<div class="slot">
		<slot />
	</div>
	<div>
	rem 수치를 사용했습니다.
	루트의 폰트 사이즈에 따라 자식의 폰트 사이즈가 변합니다.
	</div>
</div>
<style>
    .rem {
				font-size: 1rem;

        border: 0.5rem solid #000;
        border-radius: 1rem;

        padding: 1rem;
        margin-block: 1rem;
    }

    .slot {
        background-color: deepskyblue;
    }
</style>