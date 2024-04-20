<script>
	import { page } from '$app/stores';

	const pageName = $page.url.pathname.split('/').at(-2);
</script>

<h1>{pageName}</h1>

뷰 트랜지션의 애니메이션 커스터마이징 연습