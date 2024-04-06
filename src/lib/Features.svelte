<script>
    import { FEATURES } from ".";
</script>

<section id="contact" class="fw azure-bg p-0 py-5">
  <h1 class="mt-5">Siamo a disposizione per:</h1>
  <div class="flex justify-center gap-4 flex-wrap max-w-screen-lg	mx-auto py-5">
    {#each FEATURES as f}
      <div class="w-33">{f}</div>
    {/each}
  </div>
</section>