<script>
  export let day;
  export let amount;
  export let highest_amounts;
  export let active;

  const heightValue = ((amount / highest_amounts) * 100).toFixed(0);

  const classes = active ? "barchart active" : "barchart";
</script>

<div class="bar">
  <div class={classes} style="height:{heightValue}%;">
    <div class="bar-amount">${amount}</div>
  </div>
  <div class="bar-day">{day}</div>
</div>

<style>
  .bar {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    text-align: center;
    width: 2.5rem;
  }

  .barchart {
    position: relative;
    background-color: var(--p-red);
    border-radius: 0.25rem;
  }

  .barchart:hover {
    background-color: var(--p-red-hover);
    cursor: pointer;
  }

  .bar-amount {
    position: absolute;
    top: -3rem;
    left: 50%;
    transform: translateX(-50%);
    background-color: var(--n-darkbrown);
    border-radius: 0.5rem;
    padding: 0.4rem;
    color: var(--n-paleorange);
    font-weight: 700;
    opacity: 0;
    transition: opacity 300ms ease;
    pointer-events: none;
    z-index: 10;
  }

  .barchart:hover > .bar-amount {
    opacity: 1;
  }

  .active {
    background-color: var(--p-cyan);
  }

  .active:hover {
    background-color: var(--p-cyan-hover);
  }

  .bar-day {
    margin-top: 0.5rem;
    font-size: 0.9rem;
    color: var(--n-mediumbrown);
  }

  @media (max-width: 32rem) {
    .bar {
      width: 2rem;
    }
  }
</style>
