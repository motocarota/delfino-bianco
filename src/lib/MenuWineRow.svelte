<script>
  export let post;
  const [
    name, type, canteen, location, price
  ] = post ?? [];
</script>

<tr>
  {#if !price}
    <th colspan="3" class="pt-5 text-xl">{name}</th>
  {:else}
    <td><span class="text-xl">{name}</span> {type} - {canteen} - {location}</td>
    <td>{price}</td>
  {/if}
</tr>

<style>
  th {
    font-weight: 900;
  }
  td {
    text-align: left;
  }
</style>