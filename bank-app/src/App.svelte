<script>
  import Footer from "./components/Footer.svelte";
  import Header from "./components/Header.svelte";
  import Main from "./components/Main.svelte";

  let isHomePage = true;    
</script>

<main>
  <div class:backgroundAll = {isHomePage}></div>
  <Header />
  <Main />
  <Footer />
</main>

<style>
  .backgroundAll {
    position: fixed;
    height: 100%;
    width: 100%;
    background-image: url('../public/img/backgroundAll.jpg');
    background-size: contain;
    transform: scaleX(-1);
  }
</style>