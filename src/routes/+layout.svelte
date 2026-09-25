<script>
  import '../app.css';
	import Footer from '../lib/Footer.svelte';

	const jsonLd = {
		"@context": "https://schema.org",
		"@type": "Restaurant",
		name: "Delfino Bianco",
		image: "https://www.ristorantedelfinobianco.it/img/delfino.webp",
		url: "https://www.ristorantedelfinobianco.it",
		telephone: "+39-0185-450837",
		priceRange: "€€",
		servesCuisine: ["Italiana", "Ligure", "Pesce", "Pizza"],
		address: {
			"@type": "PostalAddress",
			streetAddress: "Via XX Settembre 12",
			addressLocality: "Sestri Levante",
			addressRegion: "GE",
			postalCode: "16039",
			addressCountry: "IT"
		},
		geo: {
			"@type": "GeoCoordinates",
			latitude: 44.2726976,
			longitude: 9.3952319
		},
		openingHoursSpecification: [
			{
				"@type": "OpeningHoursSpecification",
				dayOfWeek: [
					"Monday",
					"Tuesday",
					"Wednesday",
					"Thursday",
					"Friday",
					"Saturday",
					"Sunday"
				],
				opens: "17:30",
				closes: "23:00"
			}
		],
		sameAs: [
			"https://www.facebook.com/DelfinobiancoSL",
			"https://www.instagram.com/delfinobianco_",
			"https://twitter.com/delfinobianco2"
		]
	};
</script>

<svelte:head>
	{@html `<script type="application/ld+json">${JSON.stringify(jsonLd)}<\/script>`}
</svelte:head>


<div style="min-height: calc(100vh - 191px);">
  <slot></slot>
</div>
<Footer />