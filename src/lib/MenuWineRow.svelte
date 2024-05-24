<script>
  export let post;
  const [
    name, type, canteen, location, price, qty = 0, color = ""
  ] = post ?? [];
</script>

{#if qty && qty > 0}
<tr>
  {#if !price}
    <th colspan="4" class="pt-5 text-xl">{name}</th>
  {:else}
    <td style="background: {color}; width: 35px; border-radius: 30px"> </td>
    <td><span class="text-xl">{name}</span> {type} - {canteen} - {location}</td>
    <td class="price">{price}</td>
  {/if}
  </tr>
{/if}
  
<style>
  th {
    font-weight: 900;
  }
  td {
    text-align: left;
  }
  .price {
    min-width: 80px;
  }
</style>