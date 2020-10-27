<script>
  import Jumbo from "../components/Jumbo.svelte";
</script>

<style>
  h1 {
    font-weight: 800;
    font-size: 2.5em;
  }

  h2 {
    color: #1974d1;
    font-weight: 800;
  }

  p {
    font-size: 1.3em;
  }

  img {
    max-height: 200px;
  }

  .row {
    display: flex;
    flex-wrap: wrap;
    margin-bottom: 30px;
  }

  .col {
    flex: 1;
  }

  .col.image {
    text-align: center;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 3em;
    }

    .row {
      margin-bottom: 50px;
      border-bottom: solid 1px #eeeeee;
      padding-bottom: 40px;
    }

    img {
      max-height: 350px;
    }
    .col {
      flex: 1 1 25%;
      margin-right: 5%;
    }

    .cols3 .col img {
      width: 60%;
    }

    h1.subheading {
      margin-bottom: 40px;
      letter-spacing: -2px;
      font-size: 2.5em;
      color: #333333;
    }
  }
</style>

<svelte:head>
  <title>Sapper project template</title>
</svelte:head>
<Jumbo
  heading="We are Cirrus HR"
  subHeading="People's Solutions"
  image="start" />
