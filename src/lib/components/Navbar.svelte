<script>
    import { link } from "svelte-spa-router";
  </script>
  
  <nav class="bg-gray-900 text-white px-6 py-3 flex justify-between items-center">
    <div class="text-lg font-bold">AI Supply Chain</div>
    <div class="flex gap-4">
      <a use:link href="/" class="hover:text-blue-400">Dashboard</a>
      <a use:link href="/inventory" class="hover:text-blue-400">Inventory</a>
      <a use:link href="/shipments" class="hover:text-blue-400">Shipments</a>
      <a use:link href="/predictions" class="hover:text-blue-400">Predictions</a>
    </div>
  </nav>
  