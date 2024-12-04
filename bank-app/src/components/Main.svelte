<script>
  import { Router, Route, Link } from "svelte-routing";
  import Home from "../pages/Home.svelte";
  import About from "../pages/About.svelte";
  import Contact from "../pages/Contact.svelte";
</script>

<main>
  <Router>
    <Route path="/" component={Home} />
    <Route path="/about" component={About} />
    <Route path="/contact" component={Contact} />
  </Router>
</main>