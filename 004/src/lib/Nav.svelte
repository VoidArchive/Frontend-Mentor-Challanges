<script>
  import MediaQuery from "svelte-media-query";
  import snapLogo from "../assets/logo.svg";
  import Features from "./Features.svelte";
  import Company from "./Company.svelte";
</script>

<header>
  <nav>
    <img src={snapLogo} alt="snap-logo" />
    <div class="nav-left">
      <ul>
        <li><Features /></li>
        <li><Company /></li>
        <li>Careers</li>
        <li>About</li>
      </ul>
    </div>

    <div class="nav-right">
      <button class="login-btn">Login</button>
      <button class="register-btn">Register</button>
    </div>
  </nav>
</header>

<style>
  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 2rem;
  }

  .nav-left {
    display: flex;
    align-items: center;
    gap: 2rem;
  }

  ul {
    display: flex;
    align-items: center;
    list-style-type: none;
    color: var(--gray);
    gap: 2rem;
    cursor: pointer;
  }

  li:hover {
    transition: 0.5s;
    color: var(--black);
  }

  .nav-right {
    display: flex;
    align-items: center;
    gap: 2rem;
  }

  button {
    background-color: var(--white);
    color: var(--gray);
    cursor: pointer;
    transition: 0.5s;
  }

  button:hover {
    color: var(--black);
  }
  .login-btn {
    border: none;
  }

  .register-btn {
    border: 1px solid;
    border-radius: 0.9rem;
    padding: 0.5rem 1rem;
  }
</style>
