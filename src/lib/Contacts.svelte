<script>
    import { Card, Table, TableBody, TableBodyCell, TableBodyRow } from "flowbite-svelte";
    import {POSITION_LINK, ORARIO} from '../lib/index'
</script>


<section>
  <h1 class="mt-5">Contatti</h1>
  <div class="flex justify-center gap-4 flex-wrap">
    <Card>
      <h4>orario di apertura</h4>
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
    <Card href={POSITION_LINK} target="_blank">
      <img src="img/map.webp" class="rounded-lg saturation-down" alt="where"/>
    </Card>
  </div>
</section>
