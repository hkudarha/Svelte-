<script>
	// import Greet from "./components/Greet.svelte";
	// const obj = {
	// 	name:"riya",
	// 	heroname: "pari"
	// }

	import { setContext } from "svelte";
	import ComponentA  from "./components/ComponentA.svelte";
	const username= "Harsha";
	setContext('username-context', username)


	import Popup from "./components/Popup.svelte";

	let showPopup  = false;

	function closePopup (event) {
		showPopup =false
		console.log(event.detail)
	}

</script>

<main>
	<!-- <h1>Hello !</h1>
	<Greet name="harsha"  />
	<Greet name={obj.name} heroname={obj.heroname} />
	<Greet {...obj}/> -->
	<h2>App component username - {username}</h2>
	<ComponentA />

	<button on:click={() => (showPopup = true)}>Show Popup</button>
	{#if showPopup}
		<!-- <Popup on:close ={() => (showPopup =false)}/> -->
		 <Popup on:close ={closePopup} />
	{/if}
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	/* h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	} */

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>