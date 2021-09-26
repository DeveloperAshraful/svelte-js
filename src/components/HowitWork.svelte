<script>
    import { Icon } from 'sveltestrap';
    let heading = 'How it works:';
    let works = [
        {
            title: '1. Quote',
            icon: 'chat-quote',
            desc: 'Tell us what you are payment solutions you are looking for.'
        },
        {
            title: '2. Match-making',
            icon: 'share',
            desc: 'We find the most suitable payment solutions provider on the market for your business.'
        },
        {
            title: '3. Discuss',
            icon: 'shield-check',
            desc: 'The best-matched company will contact you via phone to deliver a you with a personalised quote.'
        }
    ];
</script>
<div class="wrapper-area how-area">
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="title">
          <h2>{heading}</h2>
        </div>
      </div>
    </div>
    <div class="row justify-content-center">
      {#each works as work}
      <div class="col-md-4 col-sm-6">
        <div class="how-item">
          <h3>{work.title}</h3>
          <Icon bind:name={work.icon} />
          <p>{work.desc}</p>
        </div>
      </div>
        {/each}
    </div>
  </div>
</div>
<style>
  .how-area {
    background: #E73138;
  }
  .how-item {
    text-align: center;
    padding: 0 50px;
  }
  .how-item h3 {
    font-size: 25px;
    color: #ffffff;
    margin: 0;
  }
  .how-item p {
    font-size: 14px;
    color: #ffffff;
  }

  /*============ Start Responsive ==============*/

  @media (max-width: 1200px) {
    .how-item {
      padding: 0 10px;
    }
    .how-item h3 {
      font-size: 22px;
    }
  }

  @media (max-width: 767px) {
    .how-item {
      padding: 15px 10px;
    }
  }

  @media (max-width: 575px) {
    .how-item p {
      max-width: 260px;
      margin: auto;
    }
  }

</style>