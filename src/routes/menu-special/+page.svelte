<script>
  import { onMount } from "svelte";
  import MenuSpecialRow from "../../lib/MenuSpecialRow.svelte";
  import Seo from "../../lib/Seo.svelte";
  const endpoint = "https://docs.google.com/spreadsheets/d/e/2PACX-1vRsqIM7bI1QSk4J7bJlAzgvUks8ZtzXrOSNezIQ5kYo7Cu69pcq9o4sFwX5_cnwbotWwOaSYFoVlVMA/pub?gid=2022557443&single=true&output=tsv";
  let posts = [];
  let loading = true;

  onMount(async function () {
    const response = await fetch(endpoint);
    const data = await response.text();
    
		posts = (data.split('\r\n')).map(row => row.split('\t'));
    loading = false;
  });

</script>

<Seo
  title="Menu Special - Delfino Bianco Sestri Levante"
  description="Scopri il menu special di Delfino Bianco: piatti di mare e specialità liguri del giorno a Sestri Levante."
  path="/menu-special"
  image="img/menu-word.webp"
/>

<main>
  <h1>Menu Special</h1>
  <h2>Delfino Bianco</h2>
  <img src="img/menu-word.webp" alt="menu" />
  <table>
    {#if loading}
      <p>Caricamento...</p>
    {/if}
    {#each posts as post}
      <MenuSpecialRow {post} />
    {/each}
  </table>
</main>

<style>
  main {
    text-align: center;
    background-image: url(img/leaves.webp);
    background-repeat: no-repeat;
    background-position-y: -150px;
    background-position-x: -200px;
    min-height: 600px;
    background-size: contain;
  }
  img {
    margin: 3rem auto;
  }
  table {
    width: 90%;
    margin: 3rem auto;
    border-collapse: separate;
    border-spacing: 0 1em;
  }
</style>