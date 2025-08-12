<!-- src/pages/Home.svelte -->
<script>
  import KpiCard from '../../lib/components/KpiCard.svelte';
  import ChartCard from '../../lib/components/ChartCard.svelte';

  let kpis = [
    { title: "Stock Levels", value: "82%", color: "bg-green-500" },
    { title: "On-Time Delivery", value: "95%", color: "bg-blue-500" },
    { title: "Predicted Demand", value: "+12%", color: "bg-yellow-500" }
  ];
</script>


<div class="p-6 space-y-6">
  <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
    {#each kpis as k}
      <KpiCard title={k.title} value={k.value} color={k.color} />
    {/each}
  </div>
  
  <ChartCard title="Sales vs Forecast" />
</div>
