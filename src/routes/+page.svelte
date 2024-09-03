<script>
	import About from '$lib/components/About.svelte';
	import Faq from '$lib/components/Faq.svelte';
	import Features from '$lib/components/Features.svelte';
	import Hero from '$lib/components/Hero.svelte';
</script>

<svelte:head>
	<title>Juka OS</title>
	<meta
		name="description"
		content="Discover Visual Juka OS, a custom-built operating system for the Trimui Smart Pro, designed by gamers for gamers. Experience seamless, high-performance gaming tailored to your needs."
	/>
	<meta
		name="keywords"
		content="Custom Trimui OS, TSP Custom OS, TSP OS, Trimui Smart Pro OS, Custom Firmware TSP, Custom Firmware Trimui, Trimui Smart Pro JukaOS"
	/>
</svelte:head>

<Hero />
<Features />
<About />
<Faq />
