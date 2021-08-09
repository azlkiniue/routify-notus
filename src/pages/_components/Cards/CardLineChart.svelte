<script>
  import { onMount } from "svelte";
  // library that creates chart objects in page
  import { Chart, registerables } from "chart.js";
  Chart.register(...registerables);

  // init chart
  onMount(async () => {
    var config = {
      type: "line",
      data: {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July",
        ],
        datasets: [
          {
            label: new Date().getFullYear(),
            backgroundColor: "#4c51bf",
            borderColor: "#4c51bf",
            data: [65, 78, 66, 44, 56, 67, 75],
            fill: false,
          },
          {
            label: new Date().getFullYear() - 1,
            fill: false,
            backgroundColor: "#fff",
            borderColor: "#fff",
            data: [40, 68, 86, 74, 56, 60, 87],
          },
        ],
      },
      options: {
        maintainAspectRatio: false,
        responsive: true,
        title: {
          display: false,
          text: "Sales Charts",
          fontColor: "rgba(0,0,0,0)",
        },
        tooltips: {
          mode: "index",
          intersect: false,
        },
        hover: {
          mode: "nearest",
          intersect: true,
        },
        tension: 0.3,
        plugins: {
          legend: {
            labels: {
              color: "white",
            },
            align: "end",
            position: "bottom",
          },
        },
        scales: {
          x: {
            ticks: {
              color: "rgba(255,255,255,.7)",
            },
            display: true,
            scaleLabel: {
              display: false,
              labelString: "Month",
              fontColor: "white",
            },
            grid: {
              display: false,
              borderDash: [1, 1],
              borderDashOffset: 5,
              color: "rgba(33, 37, 41, 0.3)",
            },
          },
          y: {
            ticks: {
              color: "rgba(255,255,255,.7)",
            },
            display: true,
            scaleLabel: {
              display: false,
              labelString: "Value",
              color: "white",
            },
            grid: {
              borderDash: [3, 3],
              borderDashOffset: 3,
              drawBorder: false,
              color: "rgba(255, 255, 255, 0.15)",
            },
          },
        },
      },
    };

    var ctx = document.getElementById("line-chart").getContext("2d");
    window.myLine = new Chart(ctx, config);
  });
</script>

<div
  class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded bg-blueGray-700"
>
  <div class="rounded-t mb-0 px-4 py-3 bg-transparent">
    <div class="flex flex-wrap items-center">
      <div class="relative w-full max-w-full flex-grow flex-1">
        <h6 class="uppercase text-blueGray-100 mb-1 text-xs font-semibold">
          Overview
        </h6>
        <h2 class="text-white text-xl font-semibold">Sales value</h2>
      </div>
    </div>
  </div>
  <div class="p-4 flex-auto">
    <!-- Chart -->
    <div class="relative h-350-px">
      <canvas id="line-chart" />
    </div>
  </div>
</div>
