<script>
  import dropdown from "../assets/icon-arrow-down.svg";
  import dropup from "../assets/icon-arrow-up.svg";
</script>

<button>
  Company
  <img src={dropdown} alt="dropdown" />
  <div class="dropdown-content">
    <li>History</li>
    <li>Our Team</li>
    <li>Blog</li>
  </div>
</button>

<style>
  button {
    border: none;
    background-color: var(--white);
    color: var(--gray);
  }
  button:hover .dropdown-content {
    color: var(--black);
    display: block;
  }
  img {
    margin-left: 0.5rem;
  }

  .dropdown-content {
    display: none;
    position: absolute;
    background-color: white;
  }
</style>
