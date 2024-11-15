<script>
    import Vibe from '$lib/assets/vibe.png'
    import Lillet from '$lib/assets/lillet.png'
    import Pernod from '$lib/assets/pernod.png'
    import Bacardi from '$lib/assets/bacardi.png'
    import Hendricks from '$lib/assets/hendricks.png'
    import Leonista from '$lib/assets/leonista.png'
    import London from '$lib/assets/london.png'
    import Absolut from '$lib/assets/absolut.png'
    import Cola from '$lib/assets/cocacola.png'
    import Passoa from '$lib/assets/passoa.png'
</script>

<div class="logo-container">
    <img src={Vibe} alt="Vibe Logo">
    <img src={Lillet} alt="Lillet Logo">
    <img src={Pernod} alt="Pernod Ricard Logo">
    <img src={Bacardi} alt="Bacardi Logo">
    <img src={Hendricks} alt="Hendricks Gin Logo">
    <img src={Leonista} alt="Leonista Logo">
    <img src={London} alt="The London Essence Logo">
    <img src={Absolut} alt="Absolut Vodka Logo">
    <img src={Cola} alt="Coca Cola Logo">
    <img src={Passoa} alt="Passoa Logo">
</div>

<style>
    .logo-container {
        display: inline-block;
        animation: 35s slide infinite linear;
    }
    .logo-container img {
        height: 50px;
        margin: 0 40px;
    }
     @keyframes slide {
        from {
          transform: translateX(0);
        }
        to {
          transform: translateX(-100%);
        }
    }
</style>