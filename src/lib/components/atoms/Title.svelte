<script>
  export let name = ''
  export let variant = ''
  export let size = ''
</script>

<h2 class="title title-{variant} title-{size}">
    {name}
</h2>

<style>
  .title {
    margin-bottom: 2rem;
  }

  .title-light {
    color: var(--accent2-primary);
  }
  .title-dark {
    color: var(--txt-dark-clr);
  }

  .title-s {
    font-size: var(--fs-sm);
  }

  .title-m {
    font-size: var(--fs-lg);
  }

  .title-l {
    font-size: var(--fs-2xl);
  }
</style>
