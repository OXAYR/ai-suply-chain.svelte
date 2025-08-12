<script>
  import { onMount } from 'svelte';

  let products = [];

  onMount(async () => {
    try {
      const res = await fetch('/data/products.json');
      if (!res.ok) throw new Error('Failed to load products');
      products = await res.json();
    } catch (err) {
      console.error(err);
    }
  });
</script>


<div class="p-6">
  <h1 class="text-xl font-bold mb-4">Inventory</h1>
  
  <table class="w-full bg-white shadow rounded">
    <thead>
      <tr class="bg-gray-100">
        <th class="p-2">Name</th>
        <th class="p-2">Stock</th>
        <th class="p-2">Reorder Level</th>
        <th class="p-2">Warehouse</th>
      </tr>
    </thead>
    <tbody>
      {#each products as p}
        <tr>
          <td class="p-2">{p.name}</td>
          <td class="p-2">{p.stock}</td>
          <td class="p-2">{p.reorder_level}</td>
          <td class="p-2">{p.warehouse}</td>
        </tr>
      {/each}
    </tbody>
  </table>
</div>

<style>
  table {
    border-collapse: collapse;
  }
  th, td {
    border-bottom: 1px solid #e5e7eb; /* Tailwind's gray-200 */
  }
</style>
