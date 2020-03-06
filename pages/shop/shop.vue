<template>
	<view>
		<!-- 头部 -->
		<Header></Header>
		<!-- banner -->
		<Banner></Banner>
		<!-- 位置 -->
		<Location area="商城开发"></Location>
		<!-- 类型 -->
		<ShopType :typeList="typeList"></ShopType>
		<!-- 核心技术 -->
		<ShopCore :coreList="coreList"></ShopCore>
		<!-- 相关功能 -->
		<ShopRelated></ShopRelated>
		<!-- 产品优势 -->
		<ShopAdvantage></ShopAdvantage>
		<!-- 相关案列 -->
		<ShopCase></ShopCase>
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import Banner from '../common/banner/banner'
	import Location from '../common/location/location'
	import ShopRelated from '../components/shop-related/shop-related'
	import ShopAdvantage from '../components/shop-superiority/shop-superiority'
	import ShopType from '../components/shop-type/shop-type'
	import ShopCore from '../components/shop-core/shop-core'
	import ShopCase from '../components/shop-case/shop-case'
	export default {
		data() {
			return {
				typeList:["PC商城","手机版商城","微信商城","APP"],
				coreList:[
					{
						title:"主体",
						des:"文章内容"
					},
					{
						title:"主体",
						des:"文章内容"
					},
					{
						title:"主体",
						des:"文章内容"
					}
				]
			}
		},
		components:{
			Header,
			Banner,
			Location,
			ShopRelated,
			ShopAdvantage,
			ShopType,
			ShopCore,
			ShopCase
		},
		methods: {
			
		}
	}
</script>

<style scoped>




</style>
