<script>
	import { onMount } from 'svelte'
    import CharityList from "../Components/CharityList.svelte";
	import Header from '../Components/Header.svelte'
	import Welcome from '../Components/Welcome.svelte'
	import Promo from '../Components/Promo.svelte'
	import Footer from '../Components/Footer.svelte'

	let title = "Charity";
	let charities = [];

	onMount(async function(){
		const res = await fetch('https://charity-api-bwa.herokuapp.com/charities');
		charities = await res.json();
	})
	
</script>

<body>
	<Header/>
	<Welcome/>
	<CharityList {charities}/>
	<Promo/>
	<Footer/>
</body>

<style>

</style>