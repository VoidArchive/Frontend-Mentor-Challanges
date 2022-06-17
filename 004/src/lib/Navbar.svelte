<script>
  import logo from "../assets/logo.svg";
  import MediaQuery from "svelte-media-query";
  import Hamburger from "../assets/icon-menu.svg";
  import Sidebar from "./Sidebar.svelte";
  import Features from "./Features.svelte";
  import Company from "./Company.svelte";

  export let open;
</script>

<header>
  <MediaQuery query="(max-width: 900px)" let:matches>
    {#if matches}
      <nav>
        <picture><img src={logo} alt="snap-logo" /></picture>
        <button on:click={() => (open = !open)}
          ><img src={Hamburger} alt="Hamburger Menu" /></button
        >
      </nav>
      <Sidebar bind:open />
    {:else}
      <nav>
        <div class="nav-left">
          <picture><img src={logo} alt="snap-logo" /></picture>
          <Features />
          <Company />
          <a href="/">Careers</a>
          <a href="/">About</a>
        </div>

        <div class="nav-right">
          <button>Login</button>
          <button class="btn-register">Register</button>
        </div>
      </nav>
    {/if}
  </MediaQuery>
</header>

<style>
  header {
    padding: 2rem;
  }

  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  picture {
    margin-right: 2rem;
  }
  .nav-left {
    display: flex;
    align-items: center;
    gap: 2rem;
  }

  .nav-right {
    display: flex;
    align-items: center;
    gap: 2rem;
  }

  .btn-register {
    border: 1px solid var(--gray);
    border-radius: 0.9rem;
    padding: 0.5rem 1rem;
  }

  .btn-register:hover {
    border: 1px solid var(--black);
  }
</style>
