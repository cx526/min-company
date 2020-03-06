<template>
	<view>	
		<Header></Header>
		
		
		<Location area="联系我们"></Location>
		<!-- 地址 -->
		<ConcactAddress></ConcactAddress>
		<ConcactMap :mapList="mapList"></ConcactMap>
		<button @click="checkLocation" type="primary" style="margin: 24rpx auto;width: 60%;">查看位置</button>
		<!-- 企业微信 -->
		<ConcactWx :wxList="wxList"></ConcactWx>
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import ConcactMap from '../components/concact-map/concact-map'
	import Location from '../common/location/location'
	import ConcactAddress from '../components/concact-address/concact-address'
	import ConcactWx from '../components/concact-wx/concact-wx'
	export default {
		data() {
			return {
				mapList: {
					latitude: 22.7545900000,
					longitude: 113.2692550000,
					covers: [
						{
							latitude: 22.7545900000,
							longitude: 113.2692550000,
							iconPath: '/static/images/location-icon.png',
							width: 20,
							height: 20,
						}
					]
				},
				wxList: ["企业微信","企业公众号","业务服务"]

			};
		},
		components: {
			Header,
			ConcactMap,
			Location,
			ConcactAddress,
			ConcactWx
		},
		methods: {
			checkLocation() {
							uni.openLocation({
									latitude: this.mapList.latitude,
									longitude: this.mapList.longitude,
									name: '龙光尚街1座1725',
									address: '佛山市顺德区容桂镇龙光尚街1座1725',
									success: function () {
											console.log('success');
									}
							});
			}
		}
	}
</script>

<style lang="scss">

</style>
