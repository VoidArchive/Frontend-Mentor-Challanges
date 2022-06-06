<script>
  import Advice from "./lib/Advice.svelte";
  import Dice from "./lib/Dice.svelte";
  import Footer from "./lib/Footer.svelte";

  let id;
  let quote;
  async function getAdvice() {
    const response = await fetch("https://api.adviceslip.com/advice");
    const data = await response.json();
    id = data.slip.id;
    quote = data.slip.advice;
  }
</script>

<main>
  {#if id}
    <Advice {id} {quote} />
  {:else}
    <Advice
      id={117}
      quote={`It is easy to sit up and take notice, what's difficult is getting up and
    taking actions.`}
    />
  {/if}
  <img
    class="divider-desktop"
    src="/image/pattern-divider-desktop.svg"
    alt="advice-divider"
  />
  <img
    class="divider-mobile"
    src="/image/pattern-divider-mobile.svg"
    alt="advice-divider"
  />

  <Dice {getAdvice} />
</main>
<Footer />

<style>
  /* Mobile: 375px */
  /* Desktop: 1440px */

  :root {
    --p-light-cyan: hsl(193, 38%, 86%);
    --p-neon-green: hsl(150, 100%, 66%);

    --n-grayish-blue: hsl(217, 19%, 38%);
    --n-dark-grayish-blue: hsl(217, 19%, 24%);
    --n-dark-blue: hsl(218, 23%, 16%);
  }

  :global(body) {
    background-color: var(--n-dark-blue);
    display: grid;
    place-items: center;
  }

  main {
    background-color: var(--n-dark-grayish-blue);
    max-width: 35rem;
    display: flex;
    flex-direction: column;
    padding: 2rem;
    border-radius: 1rem;
    align-items: center;
  }

  .divider-desktop {
    margin: 2rem 0;
  }

  .divider-mobile {
    display: none;
  }

  @media only screen and (max-width: 600px) {
    main {
      max-width: 22rem;
    }

    .divider-desktop {
      display: none;
    }

    .divider-mobile {
      display: block;
      margin: 2rem 0;
    }
  }
</style>
