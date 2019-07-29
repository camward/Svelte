<script>
	let value = 'Svelte'
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>if-else</h1>
<input type="text" bind:value />

{#if value.length < 5}
	<p>Длина меньше 5</p>
{:else if value.length > 10}
	<p>Длина больше 10</p>
{:else}
	<p>Длина между 5 и 10</p>
{/if}