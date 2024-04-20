<script>
	import { page } from '$app/stores';

	const pageName = $page.url.pathname.split('/').at(-2);
</script>

<h1>{pageName}</h1>

보더 이미지 넣어서 트랜지션 연습

결론, 보더에 이미지를 넣어도 뷰 트랜지션 실행시에는 이미지가 찌그러진다.