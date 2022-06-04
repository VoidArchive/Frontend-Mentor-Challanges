<script>
  export let balance;
</script>

<header>
  <div>
    <h1>My balance</h1>${balance}
  </div>

  <img src="/logo.svg" alt="Logo" />
</header>

<style>
  header {
    background-color: var(--p-red);
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 1rem;
    padding: 2rem 2rem;
    margin-bottom: 1rem;
  }

  div {
    display: grid;
    color: var(--n-paleorange);
    font-size: 1.75rem;
    font-weight: 700;
  }

  h1 {
    font-size: 0.9rem;
    font-weight: 400;
    opacity: 0.8;
    margin-bottom: 0.25rem;
  }

  img {
    height: 2.5rem;
  }

  @media (max-width: 32rem) {
    header {
      padding: 1.25rem;
    }
  }
</style>
