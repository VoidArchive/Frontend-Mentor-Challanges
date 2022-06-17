<script>
  import arrowDown from "../assets/icon-arrow-down.svg";
  import arrowUp from "../assets/icon-arrow-up.svg";

  let toggle = false;
</script>

<button on:click={() => (toggle = !toggle)}>
  Company
  {#if toggle}
    <img class="arrow" src={arrowUp} alt="arrow-Up" />
    <div class="content">
      <a href="">History</a>
      <a href="">Our Team</a>
      <a href="">Blog</a>
    </div>
  {:else}
    <img class="arrow" src={arrowDown} alt="arrow-Down" />
  {/if}
</button>

<style>
  .content {
    position: absolute;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding: 2rem 2rem;
    align-items: start;
    background-color: white;
    margin-top: 1rem;
    border-radius: 1rem;
    box-shadow: 1px 1px 1rem hsl(0, 0%, 77%);
  }

  @media screen and (max-width: 900px) {
    .content {
      position: relative;
      background-color: var(--white);
      box-shadow: none;
      border-radius: none;
      margin: 0;
    }
  }
  .arrow {
    margin-left: 0.5rem;
  }

  button {
    /* width: fit-content; */
    padding: 0;
  }
</style>
