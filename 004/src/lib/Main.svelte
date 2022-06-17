<script>
  import databiz from "../assets/client-databiz.svg";
  import audiopile from "../assets/client-audiophile.svg";
  import meet from "../assets/client-meet.svg";
  import maker from "../assets/client-maker.svg";
  import heroimgdesktop from "../assets/image-hero-desktop.png";
  import heroimgmobile from "../assets/image-hero-mobile.png";
  import MediaQuery from "svelte-media-query";
</script>

<main>
  <div class="left">
    <h1>Make remote work</h1>
    <p>
      Get your team in sync, no matter your location. Streamline processes,
      create team rituals, and watch productivity soar.
    </p>
    <button>Learn more</button>

    <div class="client">
      <img src={databiz} alt="" />
      <img src={audiopile} alt="" />
      <img src={meet} alt="" />
      <img src={maker} alt="" />
    </div>
  </div>

  <picture>
    <MediaQuery query="(max-width: 900px)" let:matches>
      {#if matches}
        <img class="hero" src={heroimgmobile} alt="hero-img" />
      {:else}
        <img class="hero" src={heroimgdesktop} alt="hero-img" />
      {/if}
    </MediaQuery>
  </picture>
</main>

<style>
  main {
    display: flex;
    align-items: end;
    gap: 4rem;
    max-width: 1200px;
    margin-inline: auto;
  }

  .hero {
    height: 45rem;
  }

  p {
    color: var(--gray);
    font-size: 18px;
    margin: 3rem 7rem 3rem 0;
    line-height: 1.5;
  }

  h1 {
    font-size: 5rem;
    margin: 0 4rem 3rem 0;
  }

  button {
    color: var(--white);
    background-color: var(--black);
    border-radius: 1rem;
    padding: 0.8rem 1.25rem;
    text-align: center;
    margin-bottom: 3rem;
  }

  button:hover {
    background-color: var(--white);
    border: 1px solid var(--black);
  }

  .client {
    margin-top: 3rem;
    display: flex;
    align-items: center;
    gap: 2rem;
  }

  @media screen and (max-width: 900px) {
    main {
      flex-direction: column-reverse;
      justify-content: center;
      align-items: center;
      margin: 3rem;
      
    }
  

    .left {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    h1 {
      font-size: 2rem;
    }
  }
</style>
