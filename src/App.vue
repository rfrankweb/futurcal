<template>
  <div id="app">
	<GridCal /> 
  </div>
</template>

<script>
import GridCal from './components/GridCal.vue'
export default {
  name: 'app',
  components: {
    GridCal 
  }
}
</script>

<style>
* {
	margin: 0;
	padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
