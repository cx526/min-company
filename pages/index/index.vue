<template>
	<view>
		<!-- 头部 -->
		<Header></Header>
		<!-- banner -->
		<Banner></Banner>
		<!-- 公告 -->
		<Notice></Notice>
		<!-- 我们的优势 -->
		<Advantage :advantageList="advantageList"></Advantage>
		<!-- 谷智产品 -->	
		<Product></Product>
		<!-- 谷智管理 -->
		<Message></Message>
		<!-- 谷智服务 -->
		<Service></Service>
		<!-- swiper -->
		<Swiper :serviceImg="serviceImg" @productArticle='productArticle'></Swiper>
		<!-- 谷智动态 -->
		<!-- 文章列表 -->
		<ArticleList :articleList="articleList"></ArticleList>
		<!-- 谷智用户 -->
		<User></User>
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import Banner from '../common/banner/banner'
	import Notice from '../components/index-notice/index-notice'
	import Title from '../components/index-title/index-title'
	import Message from '../components/index-message/index-message'
	import Swiper from '../common/swiper/swiper'
	import ArticleList from '../components/index-dynamic/index-dynamic'
	import User from '../components/index-user/index-user'
	import Service from '../components/index-service/index-service'
	import Product from '../components/index-product/index-product'
	import Advantage from '../components/index-advantage/index-advantage'
	export default {
		data() {
			return {
				bgColor: '#D4D4D4',
				// 优势数据
				advantageList: [
					{
						icon: 'icon iconfont icon-tuandui',
						title: '团队优势'
					},
					{
						icon: 'icon iconfont icon-jishuzhichi',
						title: '技术优势'
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '服务优势'
					},
					{
						icon: 'icon iconfont icon-jingyan',
						title: '经验优势'
					},
					{
						icon: 'icon iconfont icon-shouhou',
						title: '售后优势'
					},
				],
				// 轮播图模拟数据
				serviceImg:[
					"/static/images/bannerBg.jpg",
					"/static/images/loginBanner.jpg",
					"/static/images/bannerBg.jpg"
				],
				// 文章列表模拟数据
				articleList: [
					{
						topic: '/static/images/bannerBg.jpg',
						title: '文章主题',
						des: '文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明',
						time: '2020-02-20'
					},
					{
						topic: '/static/images/bannerBg.jpg',
						title: '文章主题',
						des: '文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明',
						time: '2020-02-20'
					},
					{
						topic: '/static/images/bannerBg.jpg',
						title: '文章主题',
						des: '文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明',
						time: '2020-02-20'
					},
				]
			}
		},
		components:{
			Header,
			Banner,
			Title,
			Message,
			Notice,
			Swiper,
			ArticleList,
			User,
			Service,
			Product,
			Advantage
		},
		onLoad() {

		},
		methods: {
		
			// 点击谷智服务图片跳转到文章页
			productArticle(index) {
				uni.switchTab({
					url:'/pages/develop/develop'
				})
			}
		}
	}
</script>

<style scoped>
	
</style>
