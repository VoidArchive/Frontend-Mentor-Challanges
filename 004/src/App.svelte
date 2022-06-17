<script>
  import Navbar from "./lib/Navbar.svelte";
  import Main from "./lib/Main.svelte";
  import Footer from "./lib/Footer.svelte";
  let open = false;
</script>

<div class:open />
<Navbar bind:open />
<Main />
<Footer />

<style>
  .open {
    position: fixed;
    top: 0;
    right: 0;
    width: 100%;
    height: 100vh;
    background-color: rgb(0, 0, 0, 0.5);
    transition: 0.3s;
  }
</style>
