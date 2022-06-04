<script>
  import Bar from "./Bar.svelte";
  import Total from "./Total.svelte";

  export let Data;
  export let highest_amounts;
  export let today;
  export let month_total;
  export let percentage;
</script>

<main>
  <h1>Spending - Last 7 days</h1>
  <div>
    {#each Data as data}
      <Bar
        day={data.day}
        amount={data.amount}
        {highest_amounts}
        active={today === data.day ? true : false}
      />
    {/each}
  </div>

  <hr />

  <Total {month_total} {percentage} />
</main>

<style>
  main {
    background-color: var(--n-paleorange);
    padding: 2rem 2rem;
    border-radius: 1rem;
  }

  h1 {
    margin-bottom: 3.5rem;
    font-size: 1.6rem;
    color: var(--n-darkbrown);
  }

  div {
    display: flex;
    justify-content: space-between;
    gap: 1rem;
    height: 10rem;
  }

  hr {
    margin-block: 1.75rem;
    border: none;
    border-top: 1px solid var(--n-mediumbrown);
    opacity: 0.3;
  }

  @media (max-width: 32rem) {
    main {
      padding: 1.25rem;
    }
    h1 {
      font-size: 1.25rem;
    }

    div {
      gap: 0.75rem;
    }
  }
</style>
