<script>
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
</script>

<svelte:head>
	<script type="application/ld+json">
		{
			"@context": "https://schema.org",
			"@type": "SoftwareApplication",
			"name": "Visual Juka OS",
			"operatingSystem": "Trimui Smart Pro (TSP)",
			"applicationCategory": "Operating System",
			"description": "Visual Juka OS is a custom operating system developed for the Trimui Smart Pro (TSP) handheld console, providing an intuitive interface and optimized performance for gaming and multimedia applications.",
			"softwareVersion": "1.0",
			"datePublished": "2024-09-02",
			"softwareRequirements": "Trimui Smart Pro (TSP) hardware",
			"releaseNotes": "Initial release with core gaming and multimedia support.",
			"offers": {
				"@type": "Offer",
				"price": "0",
				"priceCurrency": "USD",
				"url": "https://github.com/jukaLang"
			},
			"author": {
				"@type": "Organization",
				"name": "Juka Programming Language",
				"url": "https://os.jukalang.com"
			},
			"applicationSubCategory": "GameConsoleApplication",
			"operatingSystemRequirements": "Linux-based",
			"url": "https://os.jukalang.com",
			"image": "https://os.jukalang.com/logo.svg",
			"aggregateRating": {
				"@type": "AggregateRating",
				"ratingValue": "4.5",
				"ratingCount": "50",
				"reviewCount": "20"
			}
		}
	</script>
</svelte:head>

<Header />
<main>
	<slot></slot>
</main>
<Footer />

<style lang="scss"></style>
