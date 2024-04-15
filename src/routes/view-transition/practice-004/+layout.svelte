<script>
	import Border from '$lib/Border.svelte';
</script>

<ul>
	<li>
		<a href="a">a</a>
	</li>
	<li>
		<a href="b">b</a>
	</li>
	<li>
		<a href="c">c</a>
	</li>
</ul>

<Border>
	<slot />
</Border>
