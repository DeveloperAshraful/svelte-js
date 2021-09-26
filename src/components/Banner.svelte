<script>
    import {Icon} from 'sveltestrap';
    import Quote from "./Quote.svelte";

    let tittle = 'Compare Quotes for <br> Card Payment Solutions';
    let desc = 'A card payment solution contactless for Restaurants, Bars, Hotels and more:';
    let features = [
        {title: 'Contactless payment'},
        {title: 'Online payment'},
        {title: '12 month contract'},
        {title: 'No fee to cancel'}
    ];
</script>
<div class="banner-area">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-lg-5 col-md-12">
        <div class="banner-content">
          <h2>{@html tittle}</h2>
          <h5>{desc}</h5>
          <ul>
            {#each features as feature }
            <li><Icon name="check2" />  {feature.title}</li>
            {/each}
          </ul>
        </div>
      </div>
      <div class="col-lg-7 col-md-12">
        <Quote/>
      </div>
    </div>
  </div>
</div>
<style>
  .banner-area{
    position: relative;
    padding: 80px 0;
    background: url('../assets/images/banner-bg.jpg') no-repeat center center / cover;
  }
  .banner-area::after {
    background: linear-gradient(180deg,rgba(0,0,0,.5),rgba(0,0,0,.1));
    bottom: 0;
    content: '';
    left: 0;
    opacity: .8;
    position: absolute;
    right: 0;
    top: 0;
  }
  .banner-area > div{
    position: relative;
    z-index: 1;
  }
  .banner-content{
    position: relative;
  }
  .banner-content h2{
    font-size: 34px;
    color: #ffffff;
    font-weight: bold;
    margin-bottom: 10px;
  }
  .banner-content h5{
    font-size: 16px;
    color: #ffffff;
    line-height: 25px;
    font-weight: 600;
  }
  .banner-content ul{
    padding: 5px 0;
    margin: 0;
    list-style: none;
  }
  .banner-content li{
    font-size: 15px;
    color: #ffffff;
    font-weight: 600;
    padding: 3px 0;
  }

  /*============ Start Responsive ==============*/

  @media (max-width: 1200px) {
    .banner-content h2 {
      font-size: 30px;
    }
  }
  @media (max-width: 991px) {
    .banner-content h2 {
      font-size: 26px;
    }
    .banner-content {
      padding-bottom: 40px;
    }
  }
  @media (max-width: 767px) {}
  @media (max-width: 575px) {
    .banner-content h2 {
      font-size: 22px;
    }
  }
</style>