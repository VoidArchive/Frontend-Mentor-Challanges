<script>
  export let month_total;
  export let percentage;
</script>

<div class="Total">
  <div class="month">
    Total this month<span>${month_total}</span>
  </div>
  <div class="percent"><span>+{percentage}%</span>from last month</div>
</div>

<style>
  .Total {
    display: flex;
    justify-content: space-between;
    font-size: 0.9rem;
    color: var(--n-mediumbrown);
  }

  .Total > div {
    display: grid;
  }

  .month > span {
    color: var(--n-darkbrown);
    font-size: 2.5rem;
    font-weight: 700;
  }

  .percent {
    align-self: end;
    text-align: right;
  }

  .percent > span {
    color: var(--n-darkbrown);
    font-weight: 700;
  }

  @media (max-width: 32rem) {
    .month > span {
      font-size: 1.75rem;
    }
  }
</style>
