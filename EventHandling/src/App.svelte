<script>
	//  let count =0
	//  function increment (){
	// 	count +=1
	//  }
	//  function decrement (){
	// 	count -=1
	//  }

	const formValues ={
		name: '',
		profileSummary: '',
		country:'',
		jobLocation: [],
		remoteWork: false,
		skillSet: [],
		yearsOfExperience: ''

	}

	function submitForm(event){
		event.preventDefault()
		console.log(formValues)
	}
</script>

<main>

	<!-- <button on:click={increment}>+</button>
	<h1>{count}</h1>
	<button on:click={decrement}>-</button> -->

	<form on:submit={submitForm}>
		<div>
			<lable for="name">Name</lable>	
			<input type="text" id="name" bind:value={formValues.name}/>
		</div>

		<div>
			<label for="profile">Profile Summary</label>
			<textarea name="" id="profile" bind:value={formValues.profileSummary}/>
		</div>

		<div>
			<label for="country">Country</label>
			<select name="" id="country" bind:value={formValues.country}>  
				<option value="">Select a Country</option>
				<option value="india">India</option>
				<option value="vietnam">Vietnam</option>
				<option value="singapore">Singapore</option>
			</select>
		</div>

		<div>
			<label for="jo-location">Job Location</label>
			<select name="" id="job-location" bind:value={formValues.jobLocation} multiple>  
				<option value="">Select a Country</option>
				<option value="india">India</option>
				<option value="vietnam">Vietnam</option>
				<option value="singapore">Singapore</option>
			</select>
		</div>

		<div>
			<input 
			type="checkbox"
			id="remoteWork" 
			bind:checked={formValues.remoteWork}
			/>
			<label for="remoteWork">Open to remote work?</label>
		</div>

		<div>
			<label for="">Skill Set</label>

			<input 
			type="checkbox" 
			id="html" 
			value="html" 
			bind:group={formValues.skillSet}
			/>
			<label for="html">HTML</label>

			<input 
			type="checkbox" 
			id="css" 
			value="css"
			bind:group={formValues.skillSet}
			/>
			<label for="css">CSS</label>

			<input 
			type="checkbox" 
			id="javascript" 
			value="javascript"
			bind:group={formValues.skillSet}
			/>
			<label for="javascript">JavaScript</label>
		</div>

		<div>
			<label for="">Years Of Experience</label>

			<input 
			type="radio" 
			id="0-2" 
			value="0-2" 
			bind:group={formValues.yearsOfExperience}
			/>
			<label for="0-2">0-2</label>
			
			<input 
			type="radio" 
			id="3-5" 
			value="3-5" 
			bind:group={formValues.yearsOfExperience}
			/>
			<label for="3-5">3-5</label>

			<input 
			type="radio" 
			id="6-10" 
			value="6-10" 
			bind:group={formValues.yearsOfExperience}
			/>
			<label for="6-10">6-10</label>

			<input 
			type="radio" 
			id="10+" 
			value="10+" 
			bind:group={formValues.yearsOfExperience}
			/>
			<label for="10+">10+</label>

		</div>		

		<div>
			<button >Submit</button>
		</div>
	</form>
</main>
  
<style>
	input + label {
		display: inline-flex;	
		}
	main {
		/* text-align: center; */
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	/* h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 2em;
		font-weight: 100;
	} */

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>