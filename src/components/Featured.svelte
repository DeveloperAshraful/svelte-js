<script>
  import { Icon } from 'sveltestrap';
  let trustpilot = 'assets/images/trustpilot.jpg';
  let desc = 'We work with approved partners who have a TrustPilot score of above 4.5 to ensure you have access to the most trusted and credible payment solution providers in the U.K.';
  let features = [
      { featured: 'National UK Coverage'},
      { featured: 'Great Customer Service'},
      { featured: 'Flexible Payment Packages'},
      { featured: 'Get set up over the phone'}
  ];
</script>
<div class="wrapper-area featured-area">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-md-6 col-sm-6">
        <div class="featured-content">
          <img src={trustpilot} alt="trustpilot">
          <p>{desc}</p>
        </div>
      </div>
      <div class="col-md-6 col-sm-6">
        <div class="features">
          <ul>
            {#each features as item }
            <li> <Icon name="check-circle-fill" /> {item.featured} </li>
            {/each}
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>
<style>
  .featured-area{
    background: #fafafa;
    border-top: 5px solid #EC1F27;
  }
  .featured-content{
    text-align: center;
  }
  .featured-content img{
    max-width: 200px;
    border: 2px solid #eaeaea;
    border-radius: 5px;
    margin-bottom: 15px;
  }
  .featured-content p{
    color: #323232;
    font-size: 18px;
    max-width: 470px;
    margin: 0 auto;
  }
  .features ul{
    padding: 0 0 0 50px;
    margin: 0;
    list-style: none;
  }
  .features li{
    color: #323232;
    font-size: 18px;
    padding: 5px 0;
  }

  /*============ Start Responsive ==============*/

  @media (max-width: 767px) {
    .features ul {
      padding: 0;
    }
    .features li {
      font-size: 16px;
    }
    .featured-content p {
      font-size: 16px;
    }
  }
  @media (max-width: 575px) {
    .features ul {
      padding: 30px 0 0;
      margin: auto;
      max-width: 250px;
    }
  }

</style>