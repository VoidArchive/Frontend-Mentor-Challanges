<script>
  export let getAdvice;
</script>

<button on:click={getAdvice}>
  <img src="/image/icon-dice.svg" alt="Dice Button" />
</button>

<style>
  button {
    width: 4rem;
    height: 4rem;
    border-radius: 100%;
    border: none;
    background-color: var(--p-neon-green);
    margin-bottom: -4rem;
  }

  button:hover {
    box-shadow: 0 0 12px 1px var(--p-neon-green);
    animation: spin 2s linear infinite;
  }

  @keyframes spin {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
</style>
