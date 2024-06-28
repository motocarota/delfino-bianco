<script>
  import { onMount } from "svelte";
  import { Card } from "flowbite-svelte";
  const links = [
    { id: "menu", label: "La Carta", link: "files/menu.pdf" },
    { id: "pizza", label: "La Pizzeria", link: "files/pizza.pdf" },
    { id: "bar", label: "Bar Menú & Cocktail", link: "files/bar.pdf" },
    { id: "wine", label: "Carta del Vino", link: "menu-vini" },
    { id: "birre", label: "Carta delle Birre", link: "files/birre.pdf" },
    {
      id: "special",
      label: "Special del giorno - Lo Chef consiglia",
      link: "menu-special",
    },
  ];
  // fetch menu config
  const endpoint =
    "https://docs.google.com/spreadsheets/d/e/2PACX-1vRsqIM7bI1QSk4J7bJlAzgvUks8ZtzXrOSNezIQ5kYo7Cu69pcq9o4sFwX5_cnwbotWwOaSYFoVlVMA/pub?gid=174690761&single=true&output=tsv";
  let config = {};

  onMount(async function () {
    const response = await fetch(endpoint);
    const data = await response.text();

    config = data
      .split("\r\n")
      .map((row) => row.split("\t"))
      .reduce(
        (acc, [k, v]) => ({
          ...acc,
          [k]: v === "TRUE",
        }),
        {},
      );
  });
</script>

<section id="menu">
  <h1 class="mt-5">Menù</h1>
  <div class="flex justify-center gap-4 flex-wrap">
    {#each links as link}
      {#if config[link.id]}
        <Card img={`img/${link.id}.webp`} href={link.link} target="_blank"
          >{link.label}</Card
        >
      {/if}
    {/each}
  </div>
</section>
