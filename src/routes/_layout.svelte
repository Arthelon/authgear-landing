<script>
  import Nav from "../components/Nav.svelte";
  import Footer from "../components/Footer.svelte";
  import "../components/GlobalCSS.svelte";
</script>

<style>

</style>

<Nav />

<main>
  <slot />
</main>

<Footer />
