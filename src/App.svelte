<script>
	let name = 'Svelte'
	let check = true
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>{name}!</h1>
<input type="text" bind:value="{name}" />
<input type="checkbox" bind:checked="{check}" />