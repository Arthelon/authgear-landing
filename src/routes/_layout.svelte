<script>
  import Nav from "../components/Nav.svelte";
  // Following error is disabled sinec we are importing GlobalCSS component solely to include global styles
  import GlobalCSS from "../components/GlobalCSS.svelte"; // eslint-disable-line no-unused-vars

  export let segment;
</script>

<style>
  main {
    position: relative;
    max-width: 56em;
    background-color: white;
    padding: 2em;
    margin: 0 auto;
    box-sizing: border-box;
  }
</style>

<Nav {segment} />

<main>
  <slot />
</main>
