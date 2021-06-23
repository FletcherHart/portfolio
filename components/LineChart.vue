<template>
  <div>
    <div class="flex justify-center">
      <div class="bg-white rounded p-5 shadow sm:w-2/3 w-11/12">
        <canvas id="myChart"></canvas>
      </div>
    </div>
    <div class="flex flex-col items-center my-10 mx-1">
      <div class="grid grid-cols-2 gap-5 md:w-1/2 sm:w-2/3">
        <div class="flex flex-col bg-white rounded-lg p-5">
          <h2 class="text-center font-bold text-lg my-2">
            Weight Format (kg/lbs)
          </h2>
          <div class="flex h-full items-center justify-center">
            <select
              id="format"
              v-model="weightFormat"
              class="border border-black"
            >
              <option value="kg">kg</option>
              <option value="lbs">lbs</option>
            </select>
          </div>
        </div>
        <div class="bg-white rounded-lg p-5">
          <h2 class="text-center font-bold text-lg my-2">
            New Weight ({{ weightFormat }})
          </h2>
          <div class="flex gap-5 justify-center">
            <input
              id="newWeight"
              class="border border-black rounded w-16"
              type="number"
              step="0.5"
              min="0"
            />
            <button
              class="bg-green-600 p-1 rounded text-3xl"
              @click="addWeight"
            >
              <i class="bx bxs-plus-circle"></i>
            </button>
          </div>
        </div>
      </div>
      <div
        id="old"
        class="md:w-1/2 sm:w-2/3 w-full bg-white rounded-lg p-2 mt-5 mx-1"
      >
        <h2 class="text-center font-bold text-lg my-2">
          Old Weights ({{ weightFormat }})
        </h2>
        <table class="w-full">
          <tr>
            <th>Week</th>
            <th>Weight ({{ weightFormat }})</th>
            <th>Edit</th>
            <th>Delete</th>
          </tr>
          <tr
            v-for="(datum, index) in data"
            :key="index"
            class="bg-white border-t border-gray-400 p-2 rounded-lg"
          >
            <td>
              <div>Week {{ index + 1 }}</div>
            </td>
            <td>
              <input
                :id="index"
                class="border border-black rounded w-16"
                :value="datum"
              />
              ({{ weightFormat }})
            </td>
            <td>
              <button
                class="bg-green-600 p-1 rounded text-3xl"
                @click="upWeek(index)"
              >
                <i class="bx bxs-pencil"></i>
              </button>
            </td>
            <td>
              <button
                class="bg-red-600 p-1 rounded text-3xl"
                @click="delWeek(index)"
              >
                <i class="bx bxs-trash"></i>
              </button>
            </td>
          </tr>
        </table>
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
      weightFormat: 'kg',
    }
  },
  watch: {
    weightFormat() {
      this.myChart.data.datasets[0].label = 'Weight (' + this.weightFormat + ')'

      if (this.weightFormat === 'kg') {
        for (let i = 0; i < this.data.length; i++) {
          this.data[i] = Math.round((this.data[i] / 2.20462) * 1000) / 1000
        }
        document.getElementById('newWeight').value =
          Math.round(
            (document.getElementById('newWeight').value / 2.20462) * 1000
          ) / 1000
      } else {
        for (let i = 0; i < this.data.length; i++) {
          this.data[i] = Math.round(this.data[i] * 2.20462 * 1000) / 1000
        }
        document.getElementById('newWeight').value =
          Math.round(
            document.getElementById('newWeight').value * 2.20462 * 1000
          ) / 1000
      }

      this.myChart.update()
    },
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
              label: 'Weight (' + this.weightFormat + ')',
              fill: false,
              data: this.data,
              borderColor: 'rgb(75, 192, 192)',
            },
          ],
        },
        options: {
          responsive: true,
          scales: {
            y: {
              beginAtZero: true,
            },
          },
          ticks: {
            stepSize: 0.5,
          },
        },
      })
    },
    addWeight() {
      let weight = document.getElementById('newWeight').value
      if (!weight) weight = 0
      this.data.push(weight)
      this.labels.push('Week ' + this.data.length)
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
  min-width: 60%;
}

input {
  padding: 0.5rem;
}

td {
  text-align: center;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}
</style>
