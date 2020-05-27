<script>
  import Nav from "../components/Nav.svelte";
  import Footer from "../components/Footer.svelte";
</script>

<style global src="../styles/global.css">

</style>

<Nav />

<main>
  <slot />
</main>

<Footer />
