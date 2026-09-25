<script>
  import Navigation from "../lib/Navigation.svelte";
  import Menus from "../lib/Menus.svelte";
  import Gallery from "../lib/Gallery.svelte";
  import Features from "../lib/Features.svelte";
  import Contacts from "../lib/Contacts.svelte";
  import FwImage from "../lib/FWImage.svelte";
  import Seo from "../lib/Seo.svelte";
</script>

<Seo
  title="Delfino Bianco - Ristorante, Pizzeria e Bar a Sestri Levante"
  description="Ristorante, pizzeria e bar a due passi dalla Baia delle Favole a Sestri Levante, nel cuore della Riviera Ligure. Cucina di mare, pizza e aperitivi vista mare."
  path="/"
  image="/img/baia-2.webp"
/>

<h1 class="sr-only">
  Delfino Bianco - Ristorante, Pizzeria e Bar a Sestri Levante
</h1>

<FwImage image="bg" height={960}>
  <Navigation />
</FwImage>

<Menus />
<Gallery />
<Contacts />
<Features />
