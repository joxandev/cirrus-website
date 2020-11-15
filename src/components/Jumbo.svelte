<script>
  export let heading = "";
  export let subHeading = "";
  export let image = "";
</script>

<style>
  .jumbo {
    /* background-image: url("/images/logo-bg.png");
    background-position: -40px -80px;
    background-repeat: no-repeat; */
    background-color: rgb(13, 50, 78);
    box-sizing: border-box;
    padding: 20px 20px 5px 20px;
  }

  h1 {
    color: #ffffff;
    font-weight: 600;
    font-size: 3em;
    margin: 0;
  }

  h2 {
    font-weight: 600;
    margin: 10px 0 25px 0;
    color: #56c1ff;
  }

  .content {
    max-width: 70em;
    margin: auto;
    padding: 70px 0 30px 0;
  }

  .illustration img {
    width: 200px;
  }

  @media (min-width: 600px) {
    .jumbo{
 
          padding:0;
          display: block;
          margin-top:80px;
           
    }
    .shell {
      display: flex;
      max-width: 60em;
      align-self: center;
      padding: 0px;
      align-self:center;
      height: 300px;
    
    }

    .shell div{
   align-self: center;
    }

    .wording {
      width: 50%;
      margin-right: 2em;
    }

    .illustration img {
      width: 300px;
    }
  }
</style>

<div class="jumbo">
  <div class="shell content">
    <div class="wording">
      <h1>{heading}</h1>
      <h2>{subHeading}</h2>
    </div>
    <div class="illustration">
      <img src="/images/{image}.png" alt="start" />
    </div>

  </div>

</div>
