<template>
	<div class="date-tile" @click="createEv()">
		<p :class="selNum">{{ dateNum }}</p>
		<EventMaker v-if="evDisp" />
	</div>
</template>

<script>
	import EventMaker from './EventMaker.vue';

	export default {
		name: 'DateTile',
		components: {
			EventMaker,
		},
		data: function() {
			return {
				evDisp: false,
			};
		},
		methods: {
			createEv: function() {
				this.evDisp = true;
			},
		},
		computed: {
			selNum: function() {
				if (this.ifDate == this.dateNum) {
					return 'selCirc';
				} else {
					return '';
				}
			},
		},
		props: {
			dateNum: Number,
			ifDate: Number,
		},
	};
</script>

<style>
	.date-tile {
		width: 11rem;
		height: 9rem;
		padding: 1vh;
		border: 1px solid;
	}
	.selCirc {
		background-color: #3310af;
		color: white;
		border-radius: 1rem;
		display: inline-block;
		width: 2rem;
		height: 2rem;
		display: flex;
	}
</style>
