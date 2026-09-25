<script>
  export let image;
  export let height;
</script>

<section id="features" class="fw p-0">
  <div
    class="bg-no-repeat bg-center"
    style="background-image: url('/img/{image}.webp'); height: {height}px"
  >
    <slot />
  </div>
</section>
