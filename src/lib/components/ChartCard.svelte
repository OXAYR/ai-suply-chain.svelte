<script>
    import { onMount } from 'svelte';
    import Chart from 'chart.js/auto';
  
    export let title = "";
    let chartEl;
  
    onMount(() => {
      new Chart(chartEl, {
        type: 'line',
        data: {
          labels: ["Jan", "Feb", "Mar", "Apr", "May"],
          datasets: [
            { label: "Sales", data: [120, 150, 170, 200, 210], borderColor: "blue" },
            { label: "Forecast", data: [125, 155, 175, 205, 220], borderColor: "orange" }
          ]
        }
      });
    });
  </script>
  
  <div class="bg-white p-4 rounded shadow">
    <h2 class="font-semibold mb-4">{title}</h2>
    <canvas bind:this={chartEl}></canvas>
  </div>
  