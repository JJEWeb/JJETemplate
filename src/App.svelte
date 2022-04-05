<script>
	import Nav from './components/Nav.svelte'
	import {Router, Route} from 'svelte-navigator'

	let contactData = []


	const url = 'http://cdn.contentful.com/spaces/5o940t3dtq1j/environments/master/entries?access_token=ZKLOr10hADHsIsN-zlz23C12WuuFU3Boi0tkpud0n4A&content_type='

	const getContact = async () =>{
		const response = await fetch(url + 'contactInfo')
		const data = await response.json()
		contactData = data.items
	}
	
</script>

<Router>
	<Nav/>
	<main>
		<Route path='/'>
			<h1>Home Route</h1>
		</Route>
		<Route path='about'>
			<h1>About Route</h1>
		</Route>
		<Route path='menu'>
			<h1>Menu Route</h1>
		</Route>
		<Route path='contact'>
			<h1>Contact Us</h1>
		</Route>
	</main>

</Router>