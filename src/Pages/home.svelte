<script>
    import CharityList from "../Components/CharityList.svelte";
	import Header from '../Components/Header.svelte'
	import Welcome from '../Components/Welcome.svelte'
	import Promo from '../Components/Promo.svelte'
	import Footer from '../Components/Footer.svelte'
    import { charities } from "../Data/charities";

	let title = "Charity";
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