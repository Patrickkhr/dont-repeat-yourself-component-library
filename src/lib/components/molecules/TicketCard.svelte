<script>
  import {
    Image,
    RouteIcon,
    CocktailIcon,
    ArrowRightShort,
    Button,
  } from "$lib/index";
  export let itemCollection;
  const items = itemCollection.componentsCollection.items;
</script>

{#each items as item}
  <article>
    <div class="card-header">
      <p>
        <svg
          class="location"
          width="16"
          height="16"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M12 22C11.7667 22 11.5667 21.9333 11.4 21.8C11.2333 21.6667 11.1083 21.4917 11.025 21.275C10.7083 20.3417 10.3083 19.4667 9.825 18.65C9.35833 17.8333 8.7 16.875 7.85 15.775C7 14.675 6.30833 13.625 5.775 12.625C5.25833 11.625 5 10.4167 5 9C5 7.05 5.675 5.4 7.025 4.05C8.39167 2.68333 10.05 2 12 2C13.95 2 15.6 2.68333 16.95 4.05C18.3167 5.4 19 7.05 19 9C19 10.5167 18.7083 11.7833 18.125 12.8C17.5583 13.8 16.9 14.7917 16.15 15.775C15.25 16.975 14.5667 17.975 14.1 18.775C13.65 19.5583 13.275 20.3917 12.975 21.275C12.8917 21.5083 12.7583 21.6917 12.575 21.825C12.4083 21.9417 12.2167 22 12 22ZM12 11.5C12.7 11.5 13.2917 11.2583 13.775 10.775C14.2583 10.2917 14.5 9.7 14.5 9C14.5 8.3 14.2583 7.70833 13.775 7.225C13.2917 6.74167 12.7 6.5 12 6.5C11.3 6.5 10.7083 6.74167 10.225 7.225C9.74167 7.70833 9.5 8.3 9.5 9C9.5 9.7 9.74167 10.2917 10.225 10.775C10.7083 11.2583 11.3 11.5 12 11.5Z"
            fill="#1D1B20"
          />
        </svg>
        {item.location}
      </p>
      <p class="cocktail-price">{item.price}</p>
    </div>
    <div class="img-overlay">
      <img
        src={item.image.url}
        alt={item.image.title}
        brdRadius="var(--radius-lg)"
        opacity="0.6"
        loading="lazy"
        width="450"
        height="321"
      />
      <h2>{item.title}</h2>
    </div>
    <div class="card-description">
      <ul>
        <li>
          <span
            ><RouteIcon
              width="20"
              height="20"
              fill="var(--page-bg-color)"
            /></span
          >
          {item.location}
        </li>
        <li>
          <span
            ><CocktailIcon
              width="20"
              height="20"
              fill="var(--page-bg-color)"
            /></span
          >
          {item.cocktailDescription}
        </li>
      </ul>
    </div>

    <div class="card-buttons">
      <Button
        type="button"
        variant="tertiary"
        title="Boek nu"
        icon={RouteIcon}
        iconColor="var(--txt-quaternary-clr)"
        size="s"
      />
      <Button
        href="/home/{item.slug}"
        variant="secondary"
        title="Lees Meer"
        icon={ArrowRightShort}
        size="s"
      />
    </div>
  </article>
{/each}

<style>
  .card-header {
    display: flex;
    justify-content: space-between;
    padding: 0.5em;
  }

  .location {
    padding-top: 0.1em;
  }

  .cocktail-price {
    border: 1px solid #3f2b21;
    border-radius: 8px;
    padding: 0.2em;
  }

  article {
    display: block;
    width: 100%;
    max-width: 350px;
    /* height: 425px; */
    border: 1px solid #ccc;
    /* padding: 15px; */
    border-radius: 8px;
    background-color: #ffe5d9;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }

  @media screen and (min-width: 768px) {
    article {
      width: 80%;
      max-width: 350px;
    }
  }

  article img {
    position: relative;
    background-color: black;
    display: block;
    object-fit: cover;
    width: 350px;
    height: 250px;
    filter: brightness(0.5);
  }

  h2 {
    bottom: 5em;
    font-size: 20px;
    padding-left: 0.5em;
    padding-top: 0.5em;
  }

  .card-description {
    padding-left: 0.5em;
  }

  li {
    padding-top: 0.4em;
  }

  .card-buttons {
    width: 100%;
    display: flex;
    flex-direction: column;
    transform: scale(0.9);
    margin: 1em 1.5em 1em 0;
    gap: 1em;
  }

  @media screen and (min-width: 768px) {
    .card-buttons {
      flex-direction: unset;
      transform: none;
      margin: 1em 1.6em 1em 1.6em;
      padding-right: 15px;
      /* padding-left: 1.5em; */
      gap: 2em;
    }
  }
  span {
    padding-left: 0.5em;
  }
</style>
