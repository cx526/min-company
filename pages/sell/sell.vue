<template>
	<view>
		<Header></Header>
		<Banner></Banner>
		<Location area="直销系统"></Location>
		<SellSystem :systemList="systemList"></SellSystem>
		<SellType :typeList="typeList"></SellType>
		<SellService :serviceList="serviceList"></SellService>
		<SellNew :newList="newList"></SellNew>
		<SellArticle :articleList="articleList"></SellArticle>
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import Banner from '../common/banner/banner'
	import Location from '../common/location/location'
	import SellSystem from '../components/sell-system/sell-system'
	import SellType from '../components/sell-type/sell-type'
	import SellService from '../components/sell-service/sell-service'
	import SellNew from '../components/sell-new/sell-new'
	import SellArticle from '../components/sell-article/sell-article'
	export default {
		data() {
			return {
				
				systemList: [
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '我是文章主题',
						des: '我是文章概述'
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '我是文章主题',
						des: '我是文章概述'
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '我是文章主题',
						des: '我是文章概述'
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '我是文章主题',
						des: '我是文章概述'
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '我是文章主题',
						des: '我是文章概述'
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '我是文章主题',
						des: '我是文章概述'
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '我是文章主题',
						des: '我是文章概述'
					},
					{
						icon: 'icon iconfont icon-weibiaoti-',
						title: '我是文章主题',
						des: '我是文章概述'
					}
				],
				typeList: [
					{
						// 图标背景色
						imgBg: '#90D81F',
						// 按钮边框字体颜色
						topBg: '#A4E938',
						title: '电脑PC',
						des: '针对各类需求客户提供PC版直销系统，提供高端型商城直销网站定制开发服务。',
						icon: 'icon iconfont icon-yuanma'
					},
					{
						imgBg: '#2A9BE1',
						topBg: '#3998EA',
						title: '手机WAP',
						des: '帮助企业布局移动搜索市场，“掌控”时代，让手机用户爱上您的网站。',
						icon: 'icon iconfont icon-shouji'
					},
					{
						imgBg: '#54CAD8',
						topBg: '#4CD8E7',
						title: '安卓APP',
						des: ' 覆盖多种智能终端，抢占70%移动市场，移动互联网变现之道。',
						icon: 'icon iconfont icon-anzhuo'
					},
					{
						imgBg: '#F1BE41',
						topBg: '#F0BD40',
						title: '苹果APP',
						des: '专注中高端IOS系统开发，提供优质的IOS APP开发设计方案服务。',
						icon: 'icon iconfont icon-pingguo'
					},
					{
						imgBg: '#F7DC45',
						topBg: '#F4E45B',
						title: '微信公众号',
						des: '提供个性化定制的微信公众号开发服务，快速提高企业知名度，为您打造为品牌。',
						icon: 'icon iconfont icon-weixin'
					},
					{
						imgBg: '#FD918F',
						topBg: '#F87271',
						title: '微信小程序',
						des: '借助微信实现裂变传播的小程序商城，带来原生商城app流畅体验。',
						icon: 'icon iconfont icon-xiaochengxu'
					},	
				],
				serviceList: [
					{
						title: '视觉营销服务',
						icon: 'icon iconfont icon-weibiaoti-',
						list: [
							{
								main: '网站广告图',
								des: '提供宣传广告图专业设计'
							},
							{
								main: 'LOGO设计',
								des: '为企业定制专属标志形象'
							},
							{
								main: '网站广告图',
								des: '手册、三折页统一风格设计'
							},
							{
								main: '网站广告图',
								des: '招商、品路演、品牌宣传PPT'
							}
						]
					},
					{
						title: 'HTTPS安全服务',
						icon: 'icon iconfont icon-weibiaoti-',
						list: [
							{
								main: 'SSL证书加密',
								des: '建立访客于浏览器的加密连接'
							},
							{
								main: '绿色挂锁表示',
								des: '网站域名显示绿色挂锁'
							},
							{
								main: '安全访问',
								des: '网站信息数据深度加密'
							},
							{
								main: '账号安全',
								des: '账号不怕盗、防木马中毒'
							}
						]
					},
					{
						title: '定制开发服务',
						icon: 'icon iconfont icon-weibiaoti-',
						list: [
							{
								main: '支持任何需求开发',
								des: '十年资深技术团队、自有研发能力'
							},
							{
								main: '微商城开发/定制',
								des: '打造微商城、公众号等服务'
							},
							{
								main: 'APP开发/定制',
								des: '打造属于自己的APP商城应用'
							},
							{
								main: '小程序开发/定制',
								des: '即走即用的小程序、抢占先机'
							}
						]
					},
					{
						title: '高防/渗透',
						icon: 'icon iconfont icon-weibiaoti-',
						list: [
							{
								main: '防DDOS流量攻击',
								des: '防御一切DDOS流量攻击'
							},
							{
								main: '防CC流量攻击',
								des: '无视CC防御一键开启防御'
							},
							{
								main: '防渗透高级套件',
								des: '黑客入侵渗透，高级防御套件'
							},
							{
								main: '服务器代维',
								des: '阿里云、京东云等服务器代维'
							}
						]
					},
				],
				newList: [
					{
						imgUrl: '/static/images/bannerBg.jpg',
						des: '值此春节来临之际'
					},
					{
						imgUrl: '/static/images/bannerBg.jpg',
						des: '值此春节来临之际'
					},
					{
						imgUrl: '/static/images/bannerBg.jpg',
						des: '值此春节来临之际'
					}
				],
				articleList: [
					{
						title: '文章列表',
						time: '2020-2-22'
					},
					{
						title: '文章列表',
						time: '2020-2-22'
					},
					{
						title: '文章列表',
						time: '2020-2-22'
					}
				]
			};
		},
		components: {
			Header,
			Banner,
			Location,
			SellSystem,
			SellType,
			SellService,
			SellNew,
			SellArticle
		}
	}
</script>

<style lang="scss" scoped>
	
</style>
