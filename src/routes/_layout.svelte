<script>
  import Nav from "../components/Nav.svelte";
  import Footer from "../components/Footer.svelte";
</script>

<style global src="../styles/global.css">
  /* For information about these style tag attributes: https://github.com/sveltejs/svelte-preprocess#features */
</style>

<Nav />

<main>
  <slot />
</main>

<Footer />
