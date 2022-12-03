<template>
  <main class="col-md-9 ms-sm-auto col-lg-10 px-md-4">
    <br>
    <div class="container">
      <h1 class="mt-3 green">Forecast of SPY</h1>
      <div id="predicted_chart">
        <div class="plot">
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import * as d3 from "d3";
import * as Plot from "@observablehq/plot";
import predicted_data from '@/assets/predicted_data.json';


export default {
  name: "Predict",
  components: {},
  methods: {
    predicted() {

      var today = new Date();
      var dd = String(today.getDate()).padStart(2, '0');
      var mm = String(today.getMonth() + 1).padStart(2, '0'); //January is 0!
      var yyyy = today.getFullYear();

      today = yyyy+ '-' + mm + '-' + dd;

      var index = 0;
      while (index < 60){
        if(predicted_data[index].date === today){
          break;
        }
          index += 1;
      }

      var points = predicted_data.map(d => [new Date(d.date), d.close]);

      var sliced_points = points
      if(index > 0 && index <60){
        sliced_points = points.slice(index)
      }


      const chart = Plot.plot({
        y: {
          grid: true
        },
        marks: [
          Plot.line(sliced_points)
        ]
      });

      document.getElementById("predicted_chart").append(chart)

    },
  },
  mounted: function () {
    this.predicted();
  },
}

</script>

<style scoped>

</style>