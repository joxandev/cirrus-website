<script>
  export let segment;
</script>

<style>
  footer {
    margin: 20px auto 0 auto;
    background: rgb(13, 50, 78);
    padding: 20px 0;
  }
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
    display: flex;
    flex: 1;
    justify-content: center;
    color: white;
    font-size: 1.1em;
    font-weight: 700;
  }

  li {
    margin-right: 10px;
  }

  li.brand {
    font-size: 1.2em;
    margin-bottom: 7px;
  }

  li.brand img {
    width: 130px;
  }

  a {
    text-decoration: none;
  }

  i {
    color: #1974d1;
    font-size: 1.3em;
  }

  .social-media-icons {
    margin: 1.5em auto;
  }

  .social-media-icons li {
    margin-right: 15px;
  }

  @media (min-width: 600px) {
    ul {
      margin-top: 10px;
    }
    li {
      margin-right: 30px;
    }
    li a:hover {
      color: #1974d1;
    }
    li a {
      font-weight: 800;
    }
    .social-media-icons li {
      margin-right: 20px;
      font-size: 1.3em;
    }

    li.brand {
      font-size: 1.2em;
      margin-bottom: 15px;
    }

    li.brand img {
      width: auto;
    }
  }
</style>

<footer>
  <nav>
    <ul>
      <li class="brand">
        <a aria-current={segment === undefined ? 'page' : undefined} href=".">
          <img src="/images/reversed-logo.png" alt="start" />
        </a>
      </li>
    </ul>
    <ul>
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
          aria-current={segment === 'blog' ? 'page' : undefined}
          href="blog">
          Contact
        </a>
      </li>
    </ul>
  </nav>
  <ul class="social-media-icons">
    <li>
      <i class="fab fa-twitter" />
    </li>
    <li>
      <i class="fab fa-instagram" />
    </li>
    <li>
      <i class="fab fa-linkedin-in" />
    </li>
    <li>
      <i class="fab fa-facebook-square" />
    </li>
  </ul>
</footer>
