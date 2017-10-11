<template>
	<div class="light">
		<bulb light-color="red" 
		      v-on:bulbClicked="catchBulbCLick" />
		<bulb light-color="yellow" 
					v-on:bulbClicked="catchBulbCLick" />
		<bulb light-color="green" 
					v-on:bulbClicked="catchBulbCLick" />
	</div>
</template>

<script>
	import bulb from './bulb.vue';

	export default {
		name : 'light',
		components : {
			bulb
		},
		methods : {
			catchBulbCLick : function( color ) {
				this.$emit( 'lightClicked', color );
			}
		}
	}
</script>

<style>
	.light {
		width : 66px;
		display: block;
		border: 2px solid #000;
		background-color: #999;
		margin: auto; 
	}
</style>