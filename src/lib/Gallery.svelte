<script>
  import { Button, Carousel } from 'flowbite-svelte';

  const images = [[
    { alt: 'pizza', src: 'img/pizza-1.webp' },
    { alt: 'pizza', src: 'img/pizza-3.webp' },
    { alt: 'pizza', src: 'img/pizza-4.webp' },
    { alt: 'pizza', src: 'img/pizza-7.webp' },
  ],[
    { alt: 'dolce', src: 'img/dolce-3.webp' },
    { alt: 'dolce', src: 'img/dolce-4.webp' },
    { alt: 'dolce', src: 'img/dolce-9.webp' },
    { alt: 'dolce', src: 'img/dolce-10.webp' },
  ],[
    { alt: 'ristorante', src: 'img/risto-1.webp' },
    { alt: 'ristorante', src: 'img/risto-2.webp' },
    { alt: 'ristorante', src: 'img/risto-8.webp' },
    { alt: 'ristorante', src: 'img/risto-10.webp' },
  ],
  [
    { alt: 'locale', src: 'img/locale-1.webp' },
    { alt: 'locale', src: 'img/locale-3.webp' },
    { alt: 'locale', src: 'img/locale-7.webp' },
    { alt: 'locale', src: 'img/locale-4.webp' },
  ]
]
const sections = [
  "Pizzeria",
  // "Dolci",
  "Ristorante",
  "Location",
]
let index = 0;
let gallery = images[index];

function setIndex(i) {
  index = i;
  gallery = images[i];
}

</script>

<section id="gallery">
  <div class="flex items-center justify-center py-4 md:py-8 flex-wrap gap-3 mb-3 mx-auto">
    {#each sections as section, i}
      <Button color="light" pill size="xl" outline on:click={() => setIndex(i)}>{section}</Button>
    {/each}
  </div>

  <div class="max-w-4xl">
    <Carousel images={gallery} duration="5000" />
  </div>
</section>