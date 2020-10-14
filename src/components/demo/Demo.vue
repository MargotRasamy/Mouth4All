<template>
  <div class="demo">
    <span class="chart-container">
      <line-chart class="chart" :chart-data="generateData"></line-chart>
    </span>
    <canvas class="webgl"></canvas>
  </div>
</template>

<script>

// import * as Three from 'three'


import LineChart from '../LineChart.js'
export default {
  name: 'Demo',
  components : {
     LineChart
  },
  computed: {
      generateData(){
      var temperaturesDatas = [10, 24, 24, 36,32]
      var hoursDatas = [10, 24, 24, 36,32]

    //   this.nextDaysWeatherInfos.forEach(
    //     (forecast) => {
    //       temperaturesDatas.push(forecast.temperature)
    //       hoursDatas.push(forecast.time)
    //     }
    //   )
      
      return {
      labels: hoursDatas,
      datasets: [
          {
          label: "Score",
          borderColor: "#f39e00",
          pointBackgroundColor: "#f39e00",
          pointBorderColor: "#f39e00",
          borderWidth: 3,
          backgroundColor: "#f39e005f",
          data: temperaturesDatas
        }

        // ,{
        //   label: "Température ressentie",
        //   borderColor: "#706bff",
        //   pointBackgroundColor: "#706bff",
        //   borderWidth: 3,
        //   pointBorderColor: "#706bff",
        //   backgroundColor: "#706bff6a",
        //   data: [23.90, 20, 25.56, 31, 20, 22, 23]
        // }
        
      ]}
    } 
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/variables/colors.scss";
@import "../../assets/variables/spaces.scss";
@import "../../assets/variables/medias.scss";
@import "../../assets/variables/misc.scss";
@import "../../assets/variables/reset.scss";

.demo {
    min-height: 100vh;
    display: flex;
}

.chart-container{
  height: 400px;
  margin: auto 0;
  width: 100%;
}

.chart{
    height: 250px;
}

</style>