<script>
    export let title;
    export let value;
    export let color = "bg-blue-500";
  </script>
  
  <div class={`p-4 rounded shadow ${color} text-white`}>
    <h2 class="text-lg font-semibold">{title}</h2>
    <p class="text-2xl font-bold">{value}</p>
  </div>
  