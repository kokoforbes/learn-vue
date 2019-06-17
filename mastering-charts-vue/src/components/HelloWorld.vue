<template>
<div class="home">
  <v-chart v-bind:chartData="chartData"></v-chart>
</div>
</template>

<script>
const grades =
  [{ Name: 'Mary', s2Grade: 98, s1Grade: 95 },
   { Name: 'Sam', s2Grade: 76, s1Grade: 81 },
   { Name: 'Steve', s2Grade: 85, s1Grade: 84 },
   { Name: 'Jill', s2Grade: 87, s1Grade: 90 },
   { Name: 'Ben', s2Grade: 63, s1Grade: 75 },
   { Name: 'Brian', s2Grade: 65, s1Grade: 62 },
   { Name: 'Isabel', s2Grade: 90, s1Grade: 85 }];

export default {
  name: 'HelloWorld',
  data () {
    return {
      chartData: {
        chartType: 'barChart',
        selector: 'chart',
        title: 'Student Grades',
        subtitle: '2018 - 2019',
        width: 600,
        height: 300,
        metric: ['s1Grade', 's2Grade'],
        dim: 'Name', 
        data: grades,
        legends: {
          enabled:  true,
        },
        overrides: {
          palette: {
            fill: ['#34495E', '#4fc08d'],
            stroke: '#41B883'
          },
          x: {
            ticks: 20
            },
          y: {
            axisWidth: 40,
            }
        }
      },
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
