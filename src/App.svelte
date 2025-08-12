<script>
   import "./app.css";
   import Home from "./routes/dashboard/Home.svelte";
   const routes = {
    '/': Home,
    // '/dashboard': Dashboard
  };
</script>

<main>
  <div class=" bg-amber-600">Welcome to svelte</div>
  <a href='/dashboard'>dash</a>
</main>

<style>
  
</style>
