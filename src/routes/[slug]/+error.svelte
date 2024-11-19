<script>
  import { Button } from '$lib/index'
</script>

<section id="error">
  <div class="error-backdrop">
    <h1>404</h1>
    <p>
      "Looks like you've taken a wrong turn at the bar. This page isn't available, but 
      our cocktail menu is still on point. Let’s get you back to something delicious!"
    </p>
    <Button
      style="width: 40%;"
      href="/home" 
      variant="primary" 
      title="Back to home" 
      size="sm" 
    />
  </div>
</section>

<style>
  * {
    letter-spacing: 0.09em;
  }

  #error {
    width: 100vw;
    height: 100vh;
		display: flex;
    position: relative;
		align-items: center;
		flex-direction: column;
		justify-content: center;
    background: var(--page-bg-color);
  }

  h1 {
    font-size: 7rem;
    font-weight: 900;
    color: var(--accent2-primary);
  }

  p {
    font-size: 1.1em;
    font-weight: 600;
    color: var(--txt-quaternary-clr);
    max-width: 80ch;
    margin-bottom: 10vh;
  }
  
  .error-backdrop {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 50vh;
    z-index: 10;
  }
  .error-backdrop::before {
    position: absolute;
    content: "";
    height: 50vh;
    width: 25%;
    background: var(--accent1-tertiary);
    z-index: -10;
    left: -10%;
    border-radius: var(--radius-lg);
  }
</style>
