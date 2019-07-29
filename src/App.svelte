<script>
	let name = 'Local H1'
	let src = 'https://ru.svelte.dev/svelte-logo-horizontal.svg'
	let text = 'Local H2'
	let htmlText = '<b>Strong</b> text'
</script>

<style>
	h1 {
		color: purple;
	}
	:global(h2) {
		color: green;
	}
</style>

<h1>{name}!</h1>
<img src="{src}" alt="{text}" />
<h2>{text.toUpperCase()}!</h2>
<p>{@html htmlText}</p>