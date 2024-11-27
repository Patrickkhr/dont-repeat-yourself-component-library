<script>
    import Scenery from '$lib/assets/about-us-scenery.jpg'
    import Skyline from '$lib/assets/backdrop-skyline.png'
    import InfiniteCarrousel from '../organisms/InfiniteCarrousel.svelte'
    import Title from '../atoms/Title.svelte'

    export let items
    console.log('hello', items[2].componentsCollection)
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
  <!-- {#each items[2].componentsCollection.items as item}
    <h3>{item.title}</h3>
    <p>{item.textParagraph}</p>
  {/each} -->

  <Title 
    headertype='h2'
    content='{items[0].title}' 
    color='light' />
  <p class="initial">{items[1].textParagraph}</p>
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
