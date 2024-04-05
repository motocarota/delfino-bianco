<script>
  import { Button, Gallery } from 'flowbite-svelte';
  const images = [[
    { alt: 'pizza', src: 'img/pizza-1.webp' },
    { alt: 'pizza', src: 'img/pizza-2.webp' },
    { alt: 'pizza', src: 'img/pizza-3.webp' },
    { alt: 'pizza', src: 'img/pizza-4.webp' },
    { alt: 'pizza', src: 'img/pizza-5.webp' },
    { alt: 'pizza', src: 'img/pizza-6.webp' },
    { alt: 'pizza', src: 'img/pizza-7.webp' },
    { alt: 'pizza', src: 'img/pizza-8.webp' },
    { alt: 'pizza', src: 'img/pizza-9.webp' },
    { alt: 'pizza', src: 'img/pizza-10.webp' },
    { alt: 'pizza', src: 'img/pizza-11.webp' },
    { alt: 'pizza', src: 'img/pizza-12.webp' }
  ],[
    { alt: 'dolce', src: 'img/dolce-1.webp' },
    { alt: 'dolce', src: 'img/dolce-2.webp' },
    { alt: 'dolce', src: 'img/dolce-3.webp' },
    { alt: 'dolce', src: 'img/dolce-4.webp' },
    { alt: 'dolce', src: 'img/dolce-5.webp' },
    { alt: 'dolce', src: 'img/dolce-6.webp' },
    { alt: 'dolce', src: 'img/dolce-7.webp' },
    { alt: 'dolce', src: 'img/dolce-8.webp' },
    { alt: 'dolce', src: 'img/dolce-9.webp' },
    { alt: 'dolce', src: 'img/dolce-10.webp' },
  ],[
    { alt: 'ristorante', src: 'img/risto-1.webp' },
    { alt: 'ristorante', src: 'img/risto-2.webp' },
    { alt: 'ristorante', src: 'img/risto-3.webp' },
    { alt: 'ristorante', src: 'img/risto-4.webp' },
    { alt: 'ristorante', src: 'img/risto-5.webp' },
    { alt: 'ristorante', src: 'img/risto-6.webp' },
    { alt: 'ristorante', src: 'img/risto-7.webp' },
    { alt: 'ristorante', src: 'img/risto-8.webp' },
    { alt: 'ristorante', src: 'img/risto-9.webp' },
    { alt: 'ristorante', src: 'img/risto-10.webp' },
    { alt: 'ristorante', src: 'img/risto-11.webp' },
    { alt: 'ristorante', src: 'img/risto-12.webp' }
  ],
  [
    { alt: 'cucina', src: 'img/cucina-1.webp' },
    { alt: 'cucina', src: 'img/cucina-2.webp' },
    { alt: 'cucina', src: 'img/cucina-3.webp' },
    { alt: 'cucina', src: 'img/cucina-4.webp' },
    { alt: 'cucina', src: 'img/cucina-5.webp' },
    { alt: 'cucina', src: 'img/cucina-6.webp' },
    { alt: 'cucina', src: 'img/cucina-7.webp' },
    { alt: 'cucina', src: 'img/cucina-8.webp' },
  ]]

  let index = 0;
  let gallery = images[index];

  function setTag(i) {
    index = i;
    gallery = images[i];
  }

</script>

<section id="gallery">
  <div class="flex items-center justify-center py-4 md:py-8 flex-wrap gap-3 mb-3 mx-auto">
    <Button pill size="xl" outline on:click={() => setTag(0)}>Pizzeria</Button>
    <Button pill size="xl" outline on:click={() => setTag(1)}>Dolci</Button>
    <Button pill size="xl" outline on:click={() => setTag(2)}>Ristorante</Button>
    <Button pill size="xl" outline on:click={() => setTag(3)}>Cucina</Button>
  </div>

  <Gallery class="gap-2 grid-cols-1 md:grid-cols-2" items={gallery} />
</section>