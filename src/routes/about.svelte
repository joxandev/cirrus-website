<script>
  import Jumbo from "../components/Jumbo.svelte";
</script>

<style>
  article {
    padding: 2em 1.5em;
  }
  h1 {
    font-weight: 600;
    font-size: 2.6em;
    color: rgb(19, 49, 77);
    /* letter-spacing: -2px; */
  }

  h2 {
    font-weight: 600;
    font-size: 2.1em;
    color: #008efdff;
    margin-top: 1em;
    border-top: solid 1px #eeeeee;
    padding-top: 0.5em;
  }

  p {
    margin: 0 0 0.7em 0em;
  }
  .intro {
    font-weight: 400;
  }
</style>

<svelte:head>
  <title>About</title>
</svelte:head>

<Jumbo
  heading="About Cirrus HR"
  subHeading="Inspiring people to reach their full potential"
  image="start" />

<article>
  <h1>Who We Are?</h1>
  <p class="intro">
    We’re a friendly bunch of HR professionals, who love helping business owners
    deal with their HR issues. Whether the advice you need is regarding a
    difficult restructure, a complex TUPE transfer, or undertaking a
    disciplinary investigation you can trust that we’ll have someone with just
    the right skills in our bank of HR pro’s
  </p>
  <h2>Our Story</h2>
  <p>
    The citrusHR consultancy story is one that will ring true with a number of
    small business owners.
  </p>
  <p>
    It’s a partnership formed in 2010 by two University friends frustrated with
    the 9-5 corporate lifestyle; Kirsty Senior and Georgina Read both wanted to
    deliver more creative HR solutions for small businesses in the UK.
  </p>
  <p>
    They’ve learnt the hard way, making mistakes thanks to the challenges of the
    small business world. However they’ve also felt the elation of success –
    doubling turnover year on year whilst also somehow finding the time to bring
    babies into the world.
  </p>
  <h2>Why are we better than the rest?</h2>
  <p>
    We get to know your business from the inside out. We are passionate about
    small businesses, inspired by the ability to grow from nothing through hard
    graft and creative entrepreneurship. Whether your challenges come attached
    to reduced profits, family politics, or Trustee Board meetings we’ve usually
    been there many times before and helped overcome what on first appearance
    was impossible.
  </p>
</article>
