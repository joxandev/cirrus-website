<script>
  import Jumbo from "../../components/Jumbo.svelte";
</script>

<style>

.contactMethods{
  display: flex;
  flex-wrap: wrap;
}

.contactMethods div{
  flex: 1 1 100%;
}

 @media (min-width: 600px) {
   .contactMethods div{
  flex-basis: 30%;
  }

  .contactMethods h2{
    margin-top: .5em;
  }

 }
  
</style>

<svelte:head>
  <title>About</title>
</svelte:head>

<Jumbo
  heading="Contact Cirrus HR"
  subHeading="Got a HR query? We don't charge for a chat!"
  image="email" />

<article>
  <p class="intro">
    Curabitur at ornare nunc, ut bibendum mauris. Pellentesque sodales lectus eu dolor elementum, vel placerat odio pharetra. Cras vestibulum condimentum quam. Pellentesque a lacus ante. Nulla sed elementum erat, ut ornare dolor. Donec dictum tempus iaculis.
  </p>
 <div class="contactMethods">
  <div><h2>Email</h2></div>
  <div><h2>Mobile</h2></div>
  <div><h2>Video Call</h2></div>

 </div>
</article>
