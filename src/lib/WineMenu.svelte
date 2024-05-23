<script>
  import { Card } from "flowbite-svelte";
  const links = [
    { id: 'menu', label: 'La Carta', link: 'files/menu.pdf' },
    { id: 'pizza', label: 'La Pizzeria', link: 'files/pizza.pdf' },
    { id: 'bar', label: 'Bar Menú & Cocktail', link: 'files/bar.pdf' },
    { id: 'wine', label: 'Carta del Vino', link: 'menu-vini' },
    { id: 'special', label: 'Special del giorno - Lo Chef consiglia', link: 'menu-special' },
  ]
</script>

<section id="menu">
  <h1 class="mt-5">Menù</h1>
  <div class="flex justify-center gap-4 flex-wrap">
    {#each links as link}
      <Card img={`img/${link.id}.webp`} href={link.link} target="_blank">{link.label}</Card>
    {/each}
  </div>
</section>
