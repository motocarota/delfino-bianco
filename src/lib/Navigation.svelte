<script>
  const links = [
    { label: "Ristorante", to: "" },
    { label: "Bar", to: "" },
    { label: "Pizzeria", to: "" },
  ]
</script>

  <div class="flex justify-around max-w-[351px] mx-auto">
    {#each links as link}
      <p class="text-xl">{link.label}</p>
    {/each}
  </div>