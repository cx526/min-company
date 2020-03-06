<template>
	<view>
		<Header></Header>
		<Banner></Banner>
		<Location area="微信公众号"></Location>
		<!-- nav -->
		<WxNav :navList="navList"></WxNav>
		<WxType :typeList="typeList"></WxType>
		
		<!-- 产品优势 -->
		<WxAdvantage></WxAdvantage>
		<!-- 相关案列 -->
		<WxCase></WxCase>
		
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import Banner from '../common/banner/banner'
	import Location from '../common/location/location'
	import WxNav from '../components/wx-nav/wx-nav'
	import WxType from '../components/wx-type/wx-type'
	import WxAdvantage from '../components/wx-advantage/wx-advantage'
	import WxCase from '../components/wx-case/wx-case'
	export default {
		data() {
			return {
				navList: ["个性功能配置","专业团队开发","强大的服务支撑"],
				typeList: [
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '微信支付接口',
						main: '微信支付接口开发',
						des: '通过微信分享给好友，分享到朋友圈提高应用传播能力，你的移动应用被用户进行快速社交传播；通过接入微信支付功能，用户可以在移动应用中方便快捷的通过微信支付来付款。提高用户交互体验...',
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '网站开发',
						main: '网站开发平台',
						des: '通过接入微信登录功能，用户可使用微信帐号快速登录你的网站，降低注册门槛，提高用户留存。通过微信一键登录进行不同业务间的帐号统一。未来网站应用将会开放更多更有价值的接口和能力。',
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '微信公众帐号',
						main: '微信公众帐号开发',
						des: '公众号相比移动应用，微信公众号更容易获得用户，也更容易进行传播；通过接入微信支付功能，用户可以在公众帐号中方便快捷地通过微信支付来付款。认证服务号能够获得所有高级接口。',
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '第三方应用',
						main: '第三方平台开发',
						des: '成为第三方平台，为广大公众号提供运营服务和行业解决方案。第三方平台的开发，让公众号或小程序员运营者在面向垂直行业需求时，可以通过一键登录授权给第三方开发者，来完成相关能力。',
					},
				]
			};
		},
		components: {
			Header,
			Banner,
			Location,
			WxNav,
			WxType,
			WxAdvantage,
			WxCase
		}
	}
</script>

<style lang="scss">
	
	
</style>
