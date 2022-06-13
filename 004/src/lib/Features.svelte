<script>
  import dropdown from "../assets/icon-arrow-down.svg";
  import dropup from "../assets/icon-arrow-up.svg";
  import todo from "../assets/icon-todo.svg";
  import calender from "../assets/icon-calendar.svg";
  import reminder from "../assets/icon-reminders.svg";
  import planning from "../assets/icon-planning.svg";
</script>

<button>
  Features
  <img src={dropdown} alt="dropdown" />
  <div class="dropdown-content" />
</button>

<style>
  button {
    border: none;
    background-color: var(--white);
    color: var(--gray);
  }
  button:hover {
    color: var(--black);
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
