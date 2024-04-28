<script>
    import { Button, Card } from "flowbite-svelte";
    import {ORARIO_LINK} from '../lib/index'
    import Map from "./Map.svelte";
    import Socials from './SocialLinks.svelte'
</script>

<section>
  <h1 class="mt-5">Come trovarci:</h1>
  <Socials />
  <div class="flex justify-center gap-4 flex-wrap">
    <Card target="_blank" style="background-image: url(img/delfino.webp); background-position: center; background-size: cover;">
      <div class="py-10 mx-auto font-thin text-center">
        <h1 class="mb-4">Delfino Bianco</h1>
        
        <p>via XX Settembre 12</p>
        <p>16039 Sestri Levante (GE)</p>
        <br />
        <p>
          Tel. <a href="tel:00390185450837">+39.0185.450.837</a> -
          <a href="tel:00393281467737">328.1467737</a>
        </p>
        <p class="mb-5">
          <a href="mailto:ristorantedelfinobianco@gmail.com?subject=informazioni" target="_blank">ristorantedelfinobianco@gmail.com</a>
        </p>
        <Button color="light" href={ORARIO_LINK} target="_blank" class='my-4'>
          Visualizza Orario di Apertura
        </Button>
      </div>
    </Card>
    <Map />
    
  </div>
</section>
