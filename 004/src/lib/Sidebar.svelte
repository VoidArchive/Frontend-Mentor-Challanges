<script>
  import close from "../assets/icon-close-menu.svg";
  import Features from "./Features.svelte";
  import Company from "./Company.svelte";
  export let open;
</script>

<aside class:open>
  <button class="close-btn" on:click={() => (open = !open)}>
    <img src={close} alt="Close-menu" />
  </button>
  <nav>
    <div class="nav-left">
      <Features />
      <Company />
      <a href="##">Careers</a>
      <a href="##">About</a>
    </div>

    <div class="nav-right">
      <button>Login</button>
      <button class="btn-register">Register</button>
    </div>
  </nav>
</aside>

<style>
  aside {
    position: fixed;
    top: 0;
    width: 60%;
    height: 100vh;
    background-color: var(--white);
    right: -100%;
    transition: all 0.5s ease-in-out;
  }

  .open {
    right: 0;
  }

  .close-btn {
    position: absolute;
    top: 2rem;
    right: 2rem;
  }

  .nav-left {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 1.5rem;
    margin: 5rem 2rem;
  }

  .nav-right {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 2rem;
  }

  .btn-register {
    border: 1px solid var(--gray);
    width: 80%;
    border-radius: 1rem;
    padding: 0.8rem;
  }

  @media screen and (max-width: 400px) {
    nav {
      font-size: 0.8em;
    }
  }
</style>
