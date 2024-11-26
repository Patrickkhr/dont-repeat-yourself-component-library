<script>
    import Scenery from '$lib/assets/about-us-scenery.jpg'
    import Skyline from '$lib/assets/backdrop-skyline.png'
    import InfiniteCarrousel from '../organisms/InfiniteCarrousel.svelte'
    import Title from '../atoms/Title.svelte'
</script>

<svelte:head>
  <title>WoGo | Over ons</title>
</svelte:head>

<section id="about">
  <article>
    <Title 
      headertype='h1'
      content='Over ons' 
      color='light' />
    <blockquote class="initial">"Verken je stad, cocktail voor cocktail"</blockquote>
  </article>
  <div>
    <img src={Scenery} alt="Two people toasting">
  </div>
</section>

<section id="mission">
  <Title 
    headertype='h2'
    content='Onze Missie' 
    color='light' />
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
  <Title 
    headertype='h2'
    content='Partners' 
    color='dark' />
  <InfiniteCarrousel />
</section>

<section id="getuigenissen">
  <Title 
    headertype='h2'
    content='Getuigenissen' 
    color='light' />
  <p>WoGo is in elk geval een geweldige partner. Snel bewegend, flexibel en altijd open voor nieuwe ideeën en samenwerkingen!</p>
  <span>Timo Janse // 2022 // Eigenaar Vliegende Nederlanders en veel meer.</span>
  <img src={Skyline} alt="Cartoony skyline">
</section>


<section id="information">
  <article>
    <Title 
      headertype='h3'
      content='Kledingsvoorschriften' 
      color='dark' />
    <p class="initial">Geen strikte kledingvoorschrift, maar alsjeblieft, geen korte broek of zonnebril.</p>
  </article>

  <article>
    <Title 
      headertype='h3'
      content='Reserveringen' 
      color='dark' />
    <p class="initial">Kies een balk op de pagina Bars, en kijk welke promotie ze beschikbaar hebben!</p>
  </article>

  <article>
    <Title 
      headertype='h3'
      content='Evenementen' 
      color='dark' />
    <p class="initial">Koop tickets via onze evenementenpagina, en geniet van de lekkerste cocktails van Amsterdam.</p>
  </article>

  <article>
    <Title 
      headertype='h3'
      content='Vragen' 
      color='dark' />
    <p class="initial">Stel gerust al uw vragen, of neem contact met ons op met klachten of complimenten.</p>
  </article>
</section>

<style>
  /* Global Styling */
  * {
    text-transform: uppercase;
    line-height: 1.4;
  }
  .initial {
    text-transform: initial;
  }
  section {
    width: 100vw;
    height: 100vh;
		display: flex;
    position: relative;
		align-items: center;
		flex-direction: column;
		justify-content: center;
  }
  p:not(#information p),
  blockquote {
    font-size: 1.1em;
    font-weight: 600;
    color: var(--txt-quaternary-clr);
    max-width: 72ch;
  }
  blockquote {
    font-style: italic;
  }

  /* 'Over ons' section */
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
        width: 60vh;
        aspect-ratio: 1;
        object-fit: cover;
      }
    }
  }

  /* 'Onze missie' section */
  #mission {
    background: var(--accent1-tertiary);
  }

  /* 'Partners' section */
  #partners {
    height: fit-content;
    align-items: inherit;
    text-align: center;
    background: var(--accent2-primary);

    & h2 {
      margin: 3rem 0;
    }
  }

  /* 'Getuigenissen' section */
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

  /* 'Informatie' section */
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
  
  /* Media Query for small-screens */
  @media (max-width: 768px) {
    #about {
      flex-direction: column;
    }
    #information {
      grid-template-columns: 85%;
    }
    #information article {
      justify-self: inherit;
    }
  }
</style>
