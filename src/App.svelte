<script>
	import {onMount} from 'svelte'
	export let name;

	let contentfulData = []

	const url = 'http://cdn.contentful.com/spaces/5o940t3dtq1j/environments/master/entries?access_token=ZKLOr10hADHsIsN-zlz23C12WuuFU3Boi0tkpud0n4A&content_type=contactInfo'

	const getData = async () =>{
		const response = await fetch(url)
		const data = await response.json()
		contentfulData = data.items
		console.log(contentfulData)
	}

	getData()
	
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	{#each contentfulData as data}
		<h1>{data.fields.email}</h1>
	{/each}
</main>

<style>
	/* main {
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
	} */
</style>