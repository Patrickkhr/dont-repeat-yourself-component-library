<script>
    import { Vibe, Lillet, Pernod, Bacardi, Hendricks, London, Absolut, CocaCola, Passoa } from '$lib/assets/partners.js' 
    import Logo from "../atoms/Logo.svelte";
</script>

<ul class="logo-container"> 
  <Logo source='{Vibe}' alt='Vibe' />
  <Logo source='{Lillet}' alt='Lillet' />
  <Logo source='{Pernod}' alt='Pernod Ricard' />
  <Logo source='{Bacardi}' alt='Bacardi' />
  <Logo source='{Hendricks}' alt='Hendricks Dry Gin' />
  <Logo source='{London}' alt='The London Essence' />
  <Logo source='{Absolut}' alt='Absolut Vodka' />
  <Logo source='{CocaCola}' alt='Coca Cola' />
  <Logo source='{Passoa}' alt='Passoa' />
</ul>

<style>
  .logo-container {
    display: inline-block;
    animation: 35s slide infinite linear;
  }

  @keyframes slide {
    from {
      transform: translateX(0);
    }
    to {
      transform: translateX(-100%);
    }
  }

  @media (prefers-reduced-motion) {
    .logo-container {
      animation: none;
    }
  }
</style>