<script>
	let name = 'world';
	let stateName = $state('hi');
</script>

<input bind:value={stateName} />
<input bind:value={name} />

<h1>Hello {name}!</h1>
<h2>Hi {stateName}</h2>
