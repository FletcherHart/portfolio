<template>
  <div>
    <div class="flex justify-center">
      <div class="bg-white rounded p-5 shadow">
        <canvas id="myChart"></canvas>
      </div>
    </div>
    <div class="flex flex-col items-center my-10">
      <div class="flex flex-col">
        <h2>New Weight (kg)</h2>
        <div class="flex">
          <input id="newWeight" />
          <button @click="addWeight">Add Maxes</button>
        </div>
      </div>
      <div id="old">
        <div v-for="(datum, index) in data" :key="index">
          <input :id="index" :value="datum" />
          <button @click="upWeek(index)">Update</button>
          <button @click="delWeek(index)">Delete</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Chart from 'chart.js'

export default {
  data() {
    return {
      data: [],
      labels: [],
      myChart: Object,
    }
  },
  mounted() {
    this.updateChart()
  },
  methods: {
    updateChart() {
      const ctx = document.getElementById('myChart')
      // eslint-disable-next-line @typescript-eslint/no-unused-vars
      this.myChart = new Chart(ctx, {
        type: 'line',
        data: {
          labels: this.labels,
          datasets: [
            {
              label: 'Weight (kg)',
              fill: false,
              data: this.data,
              borderColor: 'rgb(75, 192, 192)',
            },
          ],
        },
        options: {
          responsive: true,
        },
      })
    },
    addWeight() {
      this.data.push(document.getElementById('newWeight').value)
      this.labels.push('Week ' + this.data.length)
      // for (let i = 0; i < this.data.length; i++) {
      //   this.labels[i] = 'Week ' + i
      // }
      this.myChart.update()
    },
    delWeek(index) {
      this.data.splice(index, 1)
      this.labels.pop()
      this.myChart.update()
    },
    upWeek(index) {
      this.data[index] = document.getElementById(index).value
      this.myChart.update()
    },
  },
}
</script>

<style>
canvas {
  width: 600px;
}
</style>
