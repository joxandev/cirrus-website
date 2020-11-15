<script>
  import { goto } from "@sapper/app";

  import MenuLinks from "./MenuLinks.svelte";
  export let segment;
  let menuShow = false;

  const goHome = async () => {
    console.log("Go home");
    await goto("/");
    menuShow = false;
  };

  const toggleMenu = () => {
    menuShow = !menuShow;
  };
</script>

<style>
  * {
    box-sizing: border-box;
  }
  nav {
    padding: 0 10px;
    display: flex;
    height: 70px;
    align-items: center;
    justify-content: space-between;
    position: fixed;
    background-color: #ffffff;
    top: 0;
    left: 0;
    z-index: 100;
    width: 100%;
    box-shadow: 3px -3px 5px 6px #333333;
  }
  ul {
    margin: 0;
    padding: 0;
    display: flex;
    font-weight: 800;
    list-style: none;
    color: #008efdff;
    font-size: 1.1em;
  }

  li {
    margin-right: 10px;
    font-size: 0.9em;
  }

  li.brand {
    font-size: 1.3em;
    background: url("/images/cirrus_logo.png") no-repeat;
    background-position: 10px;
    background-size: 200px auto;
    width: 210px;
    height: 60px;
  }

  li.brand a {
    display: inline-block;
    text-indent: -3000em;
    height: 100%;
    width: 100%;
  }

  a {
    text-decoration: none;
  }

  .menuLinks {
    display: none;
  }

  .burguer {
    font-size: 2.3em;
  }

  ul.menuMobile {
    padding: 40px;
    position: fixed;
    top: 70px;
    left: 0px;
    height: 100%;
    width: 90%;
    background: #008efdff;
    color: white;
    display: flex;
    flex-flow: column;
    z-index: -1;
  }

  ul.menuMobile li {
    margin-bottom: 20px;
  }

  @media (min-width: 600px) {
    li {
      margin-right: 30px;
      font-size: 1.1em;
    }

    .menuLinks {
      display: flex;
    }

    .burguer {
      display: none;
    }
  }
</style>

<nav>
  <ul>
    <li class="brand" on:click={goHome}>
      <a rel="prefetch" href=".">Cirrus HR</a>

    </li>
  </ul>

  <ul class="burguer">

    <li on:click={toggleMenu}>
      {#if !menuShow}
        <i class="fas fa-bars" />
      {:else}
        <i class="fas fa-times darkBlue" />

        <ul class="menuMobile">
          <li>
            <a rel="prefetch" href="about">About</a>
          </li>
          <li>
            <a rel="prefetch" href="services">Services</a>
          </li>
          <li>
            <a rel="prefetch" href="blog">Blog</a>
          </li>
          <li>
            <a rel="prefetch" href="contact">Contact</a>
          </li>
        </ul>
      {/if}
    </li>
  </ul>
  <ul class="menuLinks">
    <li>
      <a aria-current={segment === 'about' ? 'page' : undefined} href="about">
        About
      </a>
    </li>
    <li>
      <a
        aria-current={segment === 'services' ? 'page' : undefined}
        href="services">
        Services
      </a>
    </li>

    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
    <li>
      <a
        rel="prefetch"
        aria-current={segment === 'blog' ? 'page' : undefined}
        href="blog">
        Blog
      </a>
    </li>
    <li>
      <a
        rel="prefetch"
        aria-current={segment === 'contact' ? 'page' : undefined}
        href="contact">
        Contact
      </a>
    </li>
  </ul>
</nav>
