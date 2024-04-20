<div class="em">
	<h2>
		Dynamic Font Size -
		<slot />
	</h2>
	<div class="slot">
		<slot />
	</div>
	<div>
		em 수치를 사용했습니다.
		부모의 폰트 사이즈에 따라 자식의 폰트 사이즈가 변합니다.
	</div>
</div>
<style>
    .em {
				font-size: 1em;

        border: 0.5em solid #000;
        border-radius: 1em;

        padding: 1em;
        margin-block: 1em;
    }

    .slot {
        background-color: deepskyblue;
    }
</style>