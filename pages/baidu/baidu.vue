<template>
	<view>
		<Header></Header>
		<Banner></Banner>
		<Location area="百度小程序"></Location>
		<!-- 视频 -->
		<BaiduVideo :videoSrc="videoSrc"></BaiduVideo>
		<BaiduFeature :featureList="featureList"></BaiduFeature>
		<BaiduFlow :navList="navList"></BaiduFlow>
		<BaiduPath :pathList="pathList"></BaiduPath>
		<BaiduPlan :planList="planList"></BaiduPlan>
		<BaiduCase></BaiduCase>
		
		
		
		
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import Banner from '../common/banner/banner'
	import Location from '../common/location/location'
	import BaiduVideo from '../components/baidu-video/baidu-video'
	import BaiduFeature from '../components/baidu-feature/baidu-feature'
	import BaiduFlow from '../components/baidu-flow/baidu-flow'
	import BaiduPath from '../components/baidu-path/baidu-path'
	import BaiduPlan from '../components/baidu-plan/baidu-plan'
	import BaiduCase from '../components/baidu-case/baidu-case'
	export default {
		data() {
			return {
				videoSrc: 'https://dcloud-img.oss-cn-hangzhou.aliyuncs.com/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20181126.mp4',
				featureList: [
					{
						imgUrl: '/static/images/ability-01.jpg',
						title: '体验',
						des: '构建自然用户体验系统',
						context: '打造新时代最佳体验'
					},
					{
						imgUrl: '/static/images/ability-02.jpg',
						title: '流量',
						des: '开放百度全域千亿流量',
						context: '流量天然可运营'
					},
					{
						imgUrl: '/static/images/ability-03.jpg',
						title: '智能',
						des: 'AI 能力普及，让开发者',
						context: '重回业务理解和创意赛道'
					},
					{
						imgUrl: '/static/images/ability-04.jpg',
						title: '开放',
						des: '业界首家开放生态',
						context: '打破孤岛共建繁荣'
					}
				],
				navList: ["信息流","搜索","固定入口"],
				pathList: [
					{
						imgUrl: '/static/images/One.jpg',
						textSpcial: '注册',
						textNormal: '认证',
						des: '线上化申请入驻，快速标准的注册认证流程'
					},
					{
						imgUrl: '/static/images/Two.jpg',
						textSpcial: '创建',
						textNormal: '智能小程序',
						des: '企业小程序管理中心，高效进行智能小程序管理'
					},
					{
						imgUrl: '/static/images/Three.jpg',
						textSpcial: '开发',
						textNormal: '智能小程序',
						des: '丰富的开发者文档、标准的视觉规范指导智能小程序敏捷开发'
					},
					{
						imgUrl: '/static/images/Four.jpg',
						textSpcial: '审核',
						textNormal: '发布',
						des: '规范的审核标准，快捷的智能小程序发布上线流程'
					},
				],
				planList: [
					{
						textSpcial: '千',
						textNormal: '亿用户流量',
						des: '借助开源联盟，推动互联网从目前的封闭状态重回开放，持续为开发者拓展更多的百度内、外的流量资源。'
					},
					{
						textSpcial: '百',
						textNormal: '亿广告分成',
						des: '开发者通过把广告组件嵌入到自己的小程序里，能得到广告收益的90%。2019年这部分收益预计达到百亿。'
					},
					{
						textSpcial: '十',
						textNormal: '亿创新基金',
						des: '10亿流量资金为创新类小程序提升流量及曝光，并用更多的流量与资金推动开发者进行联合运营推广与创新孵化。'
					},
					{
						textSpcial: '一对一',
						textNormal: '专业服务',
						des: '通过线下公开课、社区、线上课程等方式，与开发者面对面交流，满足开发者在不同成长阶段的需求。'
					}
				],
				
				
				
				
			};
		},
		components: {
			Header,
			Banner,
			Location,
			BaiduVideo,
			BaiduFeature,
			BaiduFlow,
			BaiduPath,
			BaiduPlan,
			BaiduCase
		},

	}
</script>

<style lang="scss">

</style>
