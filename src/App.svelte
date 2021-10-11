<svelte:head>
  <title>Savermerchant</title>
  <link rel='icon' type='image/png' href='assets/images/favicon.png'>
  <!--  Font Family -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
  <!--  bootstrap -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/css/bootstrap.min.css">
  <!-- bootstrap Icons -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.5.0/font/bootstrap-icons.css">
</svelte:head>
<script>
    import Header from "./components/Header.svelte";
    import Footer from "./components/Footer.svelte";
    import HowitWork from "./components/HowitWork.svelte";
    import Featured from "./components/Featured.svelte";
    import Banner from "./components/Banner.svelte";
</script>
<div class="wrapper">
  <Header/>
  <Banner/>
  <Featured/>
  <HowitWork/>
  <Footer/>
</div>

