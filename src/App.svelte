<!-- <script>
	let name = "Svelte"
	let link = "https://www.google.com"
	let target = "_blank"
	let location = ""
</script>

<h1>Hello { name }!</h1>

<a href={link} target={target}>Google</a>

<br />
<input type="text" name="name" bind:value={name} />
<br />
<textarea name="location" rows="5" cols="30" bind:value={location}></textarea>
<br />
<div>{@html location}</div> -->

<!-- <script>
	let count = 0;

	function increment() {
		count++;
	}

	function decrement() {
		if (count > 0) {
			count--;
		}
	}
</script>
<h1>{count}</h1>
<br />
<button on:click={() => count++}>+</button>
<button on:click={() => {
	if (count > 0) {
		count--;
	}
}}>-</button> -->
<!-- 
<script>
	let loggedIn = false;

	function toggle() {
		loggedIn = !loggedIn;
	}
</script>

{#if loggedIn}
	<button on:click={toggle}>Logout</button>
{:else}
	<button on:click={toggle}>Login</button>
{/if} -->

<!-- <script>
	let age = 16
</script>

{#if age > 21}
	<h3>You can drink and drive but not at the same time!</h3>
{:else if age < 21 && age > 18}
	<h3>You can drive but not drink</h3>
{:else}
	<h3>You can't drive or drink</h3>
{/if} -->

<script>
	import Country from './Country.svelte';
	// let countries = ["India", "Canada", "Russia", "Nepal"]
	let countries = [
		{
			name: 'India',
			city: 'Pune'
		},
		{
			name: 'Canada',
			city: 'Waterloo'
		},
		{
			name: 'Russia',
			city: 'Moscow'
		},
		{
			name: 'Nepal',
			city: 'Pokhara'
		}
	]
</script>

<ul>
	{#each countries as country}
		<!-- <li>{country.name} - {country.city}</li> -->
		<Country country={country.name} city={country.city} />
	{/each}
</ul>