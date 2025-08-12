<script>
   import "./app.css";
   import Dashboard from "./pages/dashboard/Dashboard.svelte";
   import Router from 'svelte-spa-router';
  import Inventory from "./pages/inventory/Inventory.svelte";
  import Navbar from "./lib/components/Navbar.svelte";
   const routes = {
    '/': Dashboard,
    '/inventory': Inventory
  };
</script>

<main>
 <Navbar/>
  <Router {routes} />
</main>

<style>
  
</style>
