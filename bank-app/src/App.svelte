<script>
  import Footer from "./components/Footer.svelte";
  import Header from "./components/Header.svelte";
  import Main from "./components/Main.svelte";

  let isHomePage = true;    
</script>

<main class:backgroundAll = {isHomePage}>
  <Header />
  <Main />
  <Footer />
</main>

<style>
  .backgroundAll {
    height: 100%;
    background-image: url('../public/img/backgroundAll.jpg');
    background-size: contain;
  }
</style>