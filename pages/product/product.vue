<template>
	<view>
		<!-- 头部 -->
		<Header></Header>
		<!-- banner -->
		<Banner></Banner>
		<!-- 位置 -->
		<Location area="产品"></Location>
		<ProductNav :nav='nav' :productText='productText'></ProductNav>
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import Banner from '../common/banner/banner'
	import Location from '../common/location/location'
	import ProductNav from '../components/product-nav/product-nav'
	export default {
		data() {
			return {
				productText:["谷智CMS","微聊系统","域名主机","CPC广告"],
				nav:["谷智CMS","更新补丁","评论建议"],
				
			}
		},
		components:{
			Header,
			Banner,
			Location,
			ProductNav
		},
		methods: {
			handleNav(index) {
				this.navIndex = index
			}
		}
	}
</script>

<style scoped>

</style>
