<script>
    import { Card, Table, TableBody, TableBodyCell, TableBodyRow } from "flowbite-svelte";
    import { ORARIO } from './index'
</script>

<Card>
  <h4>Orario di Apertura</h4>
  <Table noborder={true}>
    <TableBody>
      {#each ORARIO as o}
      <TableBodyRow>
        <TableBodyCell class="text-lg py-1">{o.day} :</TableBodyCell>
        <TableBodyCell class="text-lg py-1">{o.from}</TableBodyCell>
        <TableBodyCell class="text-lg py-1">{o.to}</TableBodyCell>
      </TableBodyRow>
      {/each}
    </TableBody>
  </Table>
</Card>
