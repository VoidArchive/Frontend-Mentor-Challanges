<script>
  export let id;
  export let quote;
</script>

<div>
  <h1>ADVICE #{id}</h1>
  <blockquote>
    {quote}
  </blockquote>
</div>

<style>
  div {
    text-align: center;
  }

  h1 {
    color: var(--p-neon-green);
    margin-bottom: 2rem;
    font-size: 1rem;
    letter-spacing: 4px;
  }

  blockquote {
    color: var(--p-light-cyan);
    font-size: 28px;
  }

  @media only screen and (max-width: 600px) {
    h1 {
      font-size: 0.75rem;
    }

    blockquote {
      font-size: 1.5rem;
    }
  }
</style>
