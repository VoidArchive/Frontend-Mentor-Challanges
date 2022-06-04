<script>
  import Data from "./data/data.json";
  import Balance from "./components/Balance.svelte";
  import Chart from "./components/Chart.svelte";
  import Footer from "./components/Footer.svelte";
  const balance = 921.48;
  const month_total = 478.33;
  const percentage = 2.4;
  const amounts = Data.map((data) => data.amount);
  const highest_amounts = Math.max(...amounts);

  const weekdays = ["sun", "mon", "tue", "wed", "thu", "fri", "sat"];

  const d = new Date();
  const today = weekdays[d.getDay()];
</script>

<div>
  <Balance {balance} />
  <Chart {Data} {highest_amounts} {today} {month_total} {percentage} />
</div>

<Footer />

<style>
  :root {
    --p-red: hsl(10, 79%, 65%);
    --p-red-hover: rgb(236, 119, 95, 0.8);
    --p-cyan: hsl(186, 34%, 60%);
    --p-cyan-hover: rgba(137, 196, 203, 0.8);

    --n-darkbrown: hsl(25, 47%, 15%);
    --n-mediumbrown: hsl(28, 10%, 53%);
    --n-cream: hsl(27, 66%, 92%);
    --n-paleorange: hsl(33, 100%, 98%);
  }
  :global(body) {
    background-color: var(--n-cream);
    display: grid;
    place-items: center;
  }

  div {
    margin: 0 1rem;
  }
</style>
