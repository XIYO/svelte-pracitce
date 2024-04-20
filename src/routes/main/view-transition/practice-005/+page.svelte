<script>
	import { page } from '$app/stores';

	const pageName = $page.url.pathname.split('/').at(-2);
</script>

<h1>{pageName}</h1>

<div>
보더를 각 각 쪼개어서 뷰 트랜지션이 보더가 찌그러지 않게 하는 실험
</div>

<div>
결론 영역을 쪼개서 보더를 만드니까 영역이 움직일때 스트레치에의한 미세한 구멍이 생김, 사용 불가
</div>