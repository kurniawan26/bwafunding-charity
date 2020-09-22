<script>
	import router from 'page';
	import Home from './Pages/Home.svelte'
	import About from './Pages/About.svelte'
	import Contact from './Pages/Contact.svelte'
	import Donation from './Pages/Donation.svelte'
	import NotFound from './Pages/NotFound.svelte'

	let page, params;

	router("/", () => (page = Home));
	router("/about", () => (page = About));
	router("/contact", () => (page = Contact));
	router(
		"/donation/:id",
		(ctx, next) =>{
		params = ctx.params;
		next();
	}, 
	() => (page = Donation)
	);
	router('/*',() => (page = NotFound));
	router.start();
</script>

<svelte:component this = {page} params = {params}/>