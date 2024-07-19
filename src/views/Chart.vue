<template>
  <div>
    <Bar :chart-data="chartData" :options="chartOptions" />
  </div>
</template>

<script>
import { Bar } from 'vue-chartjs';
import { Chart as ChartJS, BarElement, CategoryScale, LinearScale, Title, Tooltip, Legend } from 'chart.js';

ChartJS.register(BarElement, CategoryScale, LinearScale, Title, Tooltip, Legend);

export default {
  name: 'BarChart',
  components: {
    Bar
  },
  data() {
    return {
      chartData: {
        labels: ['GER', 'RUS', 'BRZ', 'IND', 'CHN'],
        datasets: [
          {
            label: 'Data',
            backgroundColor: '#007bff',
            data: [200, 300, 250, 450, 600]
          }
        ]
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          y: {
            beginAtZero: true
          }
        }
      }
    };
  }
};
</script>

<style scoped>
/* You can add some styles here if needed */
</style>