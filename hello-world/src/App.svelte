<script>
	const name = 'harsha'
	const channel = '<b>Codevolution</b>'
	const hack = `<a href="#" onclick="alert('you have been hacked!')"> Win a prize!</a>`
	const id ='heading'
	const disabled = true
	// class
	const status= 'danger'
	const isPromoted = true


</script>

<main>

	<h1>Hello! {12-3}</h1>
	<div>{@html channel}</div>
	<div>{@html hack}</div>
	<h2 {id}>This is a heading</h2>
	<button {disabled}>Bind</button>

	<h2 class={status}>status</h2>

	<h2 class={isPromoted ? 'promoted' : ''}>Movie Titel</h2>

</main>

<style>
	.danger{
		color: red;
	}
	.promoted{
		font-style: italic;
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>