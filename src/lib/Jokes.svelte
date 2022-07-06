<script lang="ts">
	interface jsonData {
		error: boolean;
		setup: string;
		delivery: string;
	}

	let setupText: string = '';
	let deliveryText: string = '';

	async function getData() {
		var response = await (await fetch('https://v2.jokeapi.dev/joke/Dark?type=twopart')).json();
		const responseData: jsonData = response;
		if (!response.error) {
			setupText = responseData.setup;
			deliveryText = responseData.delivery;
		} else {
			setupText = 'An error occured.';
			deliveryText = 'Try reloading the page.';
		}
	}
</script>

<div class="joke">
	<h1>Programming Jokes</h1>
	<button id="get-joke-btn" on:click={getData}>Get a random joke</button>
	<p>{setupText}</p>
	<p>{deliveryText}</p>
</div>

<style>
	button {
		background-color: #4caf50; /* Green */
		border: none;
		color: white;
		padding: 15px 32px;
		text-align: center;
		text-decoration: none;
		display: inline-block;
		font-size: 16px;
	}
	.joke {
		text-align: center;
	}
	p {
		text-align: center;
	}
</style>
