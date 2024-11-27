<script>
    import Scenery from '$lib/assets/about-us-scenery.jpg'
    import Skyline from '$lib/assets/backdrop-skyline.png'
    import InfiniteCarrousel from '../organisms/InfiniteCarrousel.svelte'
    import Title from '../atoms/Title.svelte'

    export let items
</script>

<svelte:head>
  <title>WoGo | Over ons</title>
</svelte:head>

<section id="about">
  <article>
    <Title 
      headertype='h1'
      content='{items[0].title}' 
      color='light' />
    <blockquote class="initial">{items[0].textParagraph}</blockquote>
  </article>
  <div>
    <img src={Scenery} alt="Two people toasting">
  </div>
</section>

<section id="mission">
  <Title 
    headertype='h2'
    content='{items[1].title}' 
    color='light' />
  <p class="initial">{items[1].textParagraph}</p>
</section>

<section id="partners">
  <Title 
    headertype='h2'
    content='{items[2].title}' 
    color='dark' />
  <InfiniteCarrousel />
</section>

<section id="getuigenissen">
  <Title 
    headertype='h2'
    content='{items[3].componentsCollection.items[0].title}' 
    color='light' />
  <p>{items[3].componentsCollection.items[0].textParagraph}</p>
  <span>{items[3].componentsCollection.items[1].textParagraph}</span>
  <img src={Skyline} alt="Cartoony skyline">
</section>

<section id="information">
  <article>
    <Title 
      headertype='h3'
      content='{items[4].componentsCollection.items[0].title}' 
      color='dark' />
    <p class="initial">{items[4].componentsCollection.items[0].textParagraph}</p>
  </article>

  <article>
    <Title 
      headertype='h3'
      content='{items[4].componentsCollection.items[1].title}' 
      color='dark' />
    <p class="initial">{items[4].componentsCollection.items[1].textParagraph}</p>
  </article>

  <article>
    <Title 
      headertype='h3'
      content='{items[4].componentsCollection.items[2].title}' 
      color='dark' />
    <p class="initial">{items[4].componentsCollection.items[2].textParagraph}</p>
  </article>

  <article>
    <Title 
      headertype='h3'
      content='{items[4].componentsCollection.items[3].title}' 
      color='dark' />
    <p class="initial">{items[4].componentsCollection.items[3].textParagraph}</p>
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
