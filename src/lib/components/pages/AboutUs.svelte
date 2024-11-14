<script>
    import { Image } from '$lib/index'
    import Skyline from '$lib/assets/backdrop-skyline.png'
    import Scenery from '$lib/assets/about-us-scenery.jpg'

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

<svelte:head>
  <title>WoGo | Over ons</title>
</svelte:head>

<section id="about">
  <article>
    <h1>Over ons</h1>
    <blockquote>"Verken je stad, cocktail voor cocktail"</blockquote>
  </article>
  <div>
    <img src={Scenery} alt="Two people toasting">
  </div>
</section>

<section id="mission">
  <h2>Onze missie</h2>
  <p class="initial">
    Net als een goed gemaakte cocktail beschouwt WOGO uitgaan als een onvergetelijke ervaring. Wij willen mensen samenbrengen 
    die waarde hechten aan goede drankjes, mooie bars en vooral goed gezelschap. Onze missie is dus dat onze mensen cocktails 
    ontdekken en genieten van geweldige avonden. Daarom zoeken we voortdurend naar de beste bars en plaatsen om te bezoeken en 
    werken we samen met de beste (spirit)merken om onvergetelijke momenten te bezorgen, zodat onze klanten zich nooit zorgen 
    hoeven te maken over waar ze heen gaan! <br><br>

    WOGO is tijdens de lockdowns begonnen met haar Cocktail Walks in Amsterdam om de bars te ondersteunen en haar klanten de 
    kans te geven de stad te verkennen onder het genot van fantastische cocktails. Het doel is om deze geest voort te zetten 
    en bars en merken een podium te bieden voor zowel nieuwelingen als liefhebbers van cocktails.
  </p>
</section>

<section id="partners">
  <h2>Partners</h2>
  <div class="logos">
    <div class="logos-slide">
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
    <div class="logos-slide">
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
  </div>
</section>

<section id="getuigenissen">
  <h2>Getuigenissen & Partners</h2>
  <p>WoGo is in elk geval een geweldige partner. Snel bewegend, flexibel en altijd open voor nieuwe ideeën en samenwerkingen!</p>
  <span>Timo Janse // 2022 // Eigenaar Vliegende Nederlanders en veel meer.</span>
  <img src={Skyline} alt="Cartoony skyline">
</section>


<section id="information">
  <article>
    <h3>Kledingvoorschrift</h3>
    <p class="initial">Geen strikte kledingvoorschrift, maar alsjeblieft, geen korte broek of zonnebril.</p>
  </article>

  <article>
    <h3>Reserveringen</h3>
    <p class="initial">Kies een balk op de pagina Bars, en kijk welke promotie ze beschikbaar hebben!</p>
  </article>

  <article>
    <h3>Evenementen</h3>
    <p class="initial">Koop tickets via onze evenementenpagina, en geniet van de lekkerste cocktails van Amsterdam.</p>
  </article>

  <article>
    <h3>Vragen</h3>
    <p class="initial">Stel gerust al uw vragen, of neem contact met ons op met klachten of complimenten.</p>
  </article>
</section>

<style>
  /* ##### Global Styling ##### */
  * {
    text-transform: uppercase;
    line-height: 1.4;
  }
  .initial {
    text-transform: initial;
  }
  section {
    height: 100vh;
		display: flex;
    position: relative;
		align-items: center;
		flex-direction: column;
		justify-content: center;
  }
  h1, h2 {
    color: var(--accent2-primary);
    font-size: var(--fs-2xl);
    margin-bottom: 3rem;
  }
  h3 {
    color: var(--txt-dark-clr);
    font-size: var(--fs-xl);
  }
  p:not(#information p),
  blockquote {
    color: var(--txt-quaternary-clr);
    max-width: 72ch;
  }

  /* ##### Sections ##### */
  #about {
    flex-direction: row;

    & div, article {
      width: 50%;
      display: flex;
      align-items: center;
      flex-direction: column;
    }

    & div {
      & img {
        height: 60vh;
        aspect-ratio: 1;
        object-fit: cover;
      }
    }
  }
  #mission {
    background: var(--accent1-tertiary);
  }
  #getuigenissen {
    font-weight: bold;
    text-align: center;

    & span {
      margin-top: 2rem;
      color: var(--txt-secondary-clr);
    }
    & img {
      position: absolute;
      bottom: 0;
    }
  }
  #partners {
    height: 50vh;
    align-items: inherit;
    text-align: center;
    background: var(--accent2-primary);

    & h2 {
      color: var(--txt-dark-clr);
    }
  }
  #information {
    background: var(--accent2-primary);
    display: grid;
    grid-template-columns: 40% 40%;

    & article {
      justify-self: center;

      & p {
        max-width: 50ch;
        letter-spacing: 2px;
      }
    }
  }
  /* ##### Infinite Carrousel ##### */
  .logos {
    white-space: nowrap;
  }
  .logos:hover .logos-slide {
    animation-play-state: paused;
  }
  .logos-slide {
    display: inline-block;
    animation: 35s slide infinite linear;
  }
  .logos-slide img {
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
