<script>
	// const num=0

	// const fullname =[
	// 	{first: 'Harshita', last: 'kudarha'},
	// 	{first: 'Muskan', last: 'malviya'},
	// 	{first: 'Riya', last: 'gupta'}
	// ]


	// npm install lodash -Lodash is a predefined, third-party JavaScript utility library.
	import {shuffle} from 'lodash';
	let names =['harsha', 'lado','subh','riya'];
	const shuffleNames =() =>{
		// names = [...shuffle(names)];
		names =shuffle(names);
	};

</script>

<main>

	{#each names as name(name)}
		<h2>{name}</h2>
		<input placeholder="Last name">
	{/each}
	<div>
		<button on:click={shuffleNames}>Shuffle!</button>
	</div>

	<!-- {#if num ==0}
		<h1>Number is Zero</h1>
	{:else if num<0}
		<h1>Number is Negative</h1>
	{:else}
		<h1>Number is not Zero</h1>
	{/if} -->


	<!-- {#each fullname as name, index}
		<h2>{index +1} {name.first} {name.last}</h2>
	{/each} -->


</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		/* text-transform: uppercase; */
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>