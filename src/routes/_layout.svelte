<script>
  import Nav from "../components/Nav.svelte";
  import Footer from "../components/Footer.svelte";

  export let segment;
</script>

<style>
  * {
    box-sizing: border-box;
  }
  main {
    position: relative;
    background-color: white;
    box-sizing: border-box;
    text-align: center;
  }

  @media (min-width: 450px) {
    main {
    }
  }
</style>

<svelte:head>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.min.css" />
</svelte:head>

<Nav {segment} />

<main>
  <slot />
</main>
<Footer {segment} />
