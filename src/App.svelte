<script>
  import Router from "svelte-spa-router";
  import Game1 from "./routes/Game1.svelte";
  import Game2 from "./routes/Game2.svelte";
  import Game3 from "./routes/Game3.svelte";
  const routes = {
    '*': Game3
  }
</script>

<main class="main">
  <Router {routes} />
</main>
