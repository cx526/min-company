<template>
	<view>
		<map :latitude="mapList.latitude" :longitude="mapList.longitude" class="map" :markers="mapList.covers"></map>
	</view>
</template>

<script>
	export default {
		props: {
			mapList: {
				type: Object
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.map {
		width: 100%;
		height: 600rpx;
	}
</style>
