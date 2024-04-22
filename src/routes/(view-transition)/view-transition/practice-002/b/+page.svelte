<script>
	import Border from '$lib/view-transition/Border.svelte';
</script>

<div id="flex">
	<Border viewTransitionName="border">
		hello 나는 비
	</Border>
	<div>
		side
	</div>
</div>

<style>
    #flex {
        display: flex;
    }

    .content {
        width: 100px;
        height: 200px;
    }
</style>