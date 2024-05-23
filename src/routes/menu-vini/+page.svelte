<script>
  import { onMount } from "svelte";
  import MenuWineRow from "../../lib/MenuWineRow.svelte";
  const endpoint = "https://docs.google.com/spreadsheets/d/e/2PACX-1vRsqIM7bI1QSk4J7bJlAzgvUks8ZtzXrOSNezIQ5kYo7Cu69pcq9o4sFwX5_cnwbotWwOaSYFoVlVMA/pub?gid=0&single=true&output=tsv";
  let posts = [];
  let loading = true;

  onMount(async function () {
    const response = await fetch(endpoint);
    const data = await response.text();
    
		posts = (data.split('\r\n')).map(row => row.split('\t'));
    loading = false;
  });

</script>

<main>
  <h1>Delfino Bianco</h1>
  <h3>Carta dei vini</h3>
  <img src="img/liguria.webp" alt="liguria" />
  <table>
    {#if loading}
      <p>Caricamento...</p>
    {/if}
    {#each posts as post}
      <MenuWineRow {post} />
    {/each}
  </table>
</main>

<style>
  main {
    text-align: center;
    background-image: url(img/vino-icon2.webp);
    background-repeat: no-repeat;
    background-position-y: top;
    background-position-x: 70%;
  }
  img {
    margin: 3rem auto;
  }
  table {
    width: 90%;
    margin: auto;
    border-collapse: separate;
    border-spacing: 0 1em;
  }
</style>