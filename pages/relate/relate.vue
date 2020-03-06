<template>
	<view>
		<!-- 头部 -->
		<Header></Header>
		<!-- banner -->
		<Banner></Banner>
		<!-- 位置 -->
		<Location area="关于我们"></Location>
		<!-- nav -->
		<RelateNav :navList="navList"></RelateNav>
		<!-- 合作伙伴 -->
		<RelatePartner></RelatePartner>
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import Banner from '../common/banner/banner'
	import Location from '../common/location/location'
	import RelateNav from '../components/relate-nav/relate-nav'
	import RelatePartner from '../components/relate-partner/relate-partner'
	export default {
		data() {
			return {
				navList:["公司简介","企业文化","人才招聘","公司动态","客户评价","成功案例"],
				
			};
		},
		components:{
			Header,
			Banner,
			Location,
			RelateNav,
			RelatePartner
		},
		methods:{

		}
	}
</script>

<style lang="scss" scoped>

</style>
