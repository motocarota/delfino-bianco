<script>
  import { FooterIcon } from 'flowbite-svelte';

  const socials = [
    { id: 'fb', url: 'https://www.facebook.com/DelfinobiancoSL' },
    { id: 'ig', url: 'https://www.instagram.com/delfinobianco_' },
    { id: 'x', url: 'https://twitter.com/delfinobianco2' },
  ]
</script>
<div class="flex m-5 p-5 space-x-6 rtl:space-x-reverse sm:justify-center sm:mt-0">
  {#each socials as s}
    <FooterIcon href={s.url} target="_blank">
      <img src={`img/${s.id}.svg`} alt={s.id} width={36} height={36} />
    </FooterIcon>
  {/each}
</div>