<script>
  import { TicketCard } from "$lib/index";
  export let itemCollection;
</script>

<section class="intro">
  <h1>Tours</h1>
  <ul>
    <li>Amsterdam</li>
    <li>Rotterdam</li>
    <li>Utrecht</li>
  </ul>
</section>

<section class="tours">
  <TicketCard {itemCollection} />
</section>

<svelte:head>
  <title></title>
</svelte:head>

<style>
  .intro {
    margin-top: 8em;
    padding: 2em;
    width: auto;
    /* display: block; */
    background-color: #3f2b21;
  }

  ul {
    padding-top: 0.5em;
    display: flex;
    justify-content: center;
    list-style: none;
    flex-wrap: wrap;
  }

  li {
    color: #ffe5d9;
    cursor: pointer;
    padding: 0.5em 1em 0 2em;
  }

  li:hover {
    color: #ffaa81;
  }

  .intro ul li::after {
    content: "";
    width: 0%;
    height: 2px;
    background: #ffaa81;
    display: block;
    margin: auto;
    transition: 0.5s;
  }

  .intro ul li:hover::after {
    width: 100%;
  }

  h1 {
    text-align: center;
    color: #ffaa81;
    font-size: 3.5rem;
  }

  .tours {
    /* margin-top: 2em; */
    padding: 5em;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
  }

  /* @media screen and (min-width: 768px) {
    .tours {
      margin-top: 2em;
      display: grid;
      align-items: center;
      justify-content: center;
      gap: 20px;
    }
  } */
</style>
