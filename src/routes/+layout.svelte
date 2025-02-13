<script>
  import Footer from "$lib/Footer.svelte";
  import Navbar from "$lib/Navbar.svelte";

  let { children } = $props();
  import "../app.css";
</script>

<Navbar />

<div class="pt-16 bg-gradiente-to-b from-black to-white">
  {@render children()}
</div>

<Footer />
