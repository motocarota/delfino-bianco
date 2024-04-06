<script>
    import { Card, Table, TableBody, TableBodyCell, TableBodyRow } from "flowbite-svelte";
    import {POSITION_LINK, ORARIO} from '../lib/index'
</script>


<section>
  <h1 class="mt-5">Contatti</h1>
  <div class="flex justify-center gap-4 flex-wrap">
    <Card>
      <h4>orario di apertura</h4>
      <Table>
        <TableBody>
          {#each ORARIO as o}
          <TableBodyRow>
            <TableBodyCell class="text-lg">{o.day} :</TableBodyCell>
            <TableBodyCell class="text-lg">{o.from}</TableBodyCell>
            <TableBodyCell class="text-lg">{o.to}</TableBodyCell>
          </TableBodyRow>
          {/each}
        </TableBody>
    </Table>
    </Card>
    <Card img="img/map.webp" href={POSITION_LINK} target="_blank" class="saturation-down">
      <h4>Ristorante Delfino Bianco</h4>
      <p>via XX Settembre 12</p>
      <p>16039 Sestri Levante (Ge) ITALY</p>
      <p>Tel. +39 0185450837 - 328 1467737</p>
    </Card>
  </div>

</section>
