<script>
  import { Card } from "flowbite-svelte";
  const links = [
    { id: 'menu', label: 'La Carta' },
    { id: 'pizza', label: 'La pizzeria' },
    { id: 'bar', label: 'Bar menú & cocktail' },
    { id: 'wine', label: 'Carta del vino' },
  ]
</script>

<section id="menu">
  <h1 class="mt-5">Menù</h1>
  <div class="flex justify-center gap-4 flex-wrap">
    {#each links as link}
      <Card img={`img/${link.id}.webp`} href={`files/${link.id}.pdf`} target="_blank">{link.label}</Card>
    {/each}
  </div>
</section>
