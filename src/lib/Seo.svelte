<script>
  export let title;
  export let description;
  export let path = "/";
  export let image = "img/delfino.webp";

  const siteName = "Delfino Bianco";
  const siteUrl = "https://www.ristorantedelfinobianco.it";

  $: url = `${siteUrl}${path}`;
  $: imageUrl = `${siteUrl}/${image}`;
</script>

<svelte:head>
  <title>{title}</title>
  <meta name="description" content={description} />
  <link rel="canonical" href={url} />

  <meta property="og:type" content="website" />
  <meta property="og:site_name" content={siteName} />
  <meta property="og:locale" content="it_IT" />
  <meta property="og:title" content={title} />
  <meta property="og:description" content={description} />
  <meta property="og:url" content={url} />
  <meta property="og:image" content={imageUrl} />

  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content={title} />
  <meta name="twitter:description" content={description} />
  <meta name="twitter:image" content={imageUrl} />
</svelte:head>
