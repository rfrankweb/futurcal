<template>
  <div class="app-container">
	<!--// futurcal name in the top corner-->
	<h1 id = "app-name">Futurcal</h1>
	<!--// have a component that is the date tiles-->
	<div id = "calendar-container">
		<div v-for = "n in 28" v-bind:key = "n"  >
			<DateTile :dateNum = "n" :ifDate = 'dayDate' />
		</div>
	</div>
  </div>
</template>

<script>
import DateTile from "./DateTile.vue"

let curDate = new Date()

export default {
  name: 'CalGrid',
	data: function() {
		return {
			curDate: new Date(),
			dayDate: curDate.getDate()
		}
	},
  props: {
    msg: String
  },
	components: {
		DateTile,
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	#calendar-container {
		display: flex;
		flex-wrap: wrap;
	}
	.shaded-tile {
	}
</style>
