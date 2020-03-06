<template>
	<!-- 公共头部 -->
	<view class="header-box">
		<image src="/static/images/companyLogo.png"></image>
		<text class="icon iconfont icon-menu-two" @click="handleListShow()"></text>
		<!-- 下拉框 -->
		<template v-if="isListShow">
			<view class="select-box animated fadeIn">
				<view class="select-item" v-for="(item,index) in list" :key="index" @click="handleType(item)">{{item.name}}</view>
			</view>
		</template>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isListShow: false,
				list:[
					{
						name:'产品中心',
						url: '/pages/product/product',
						type: true
					},
					{
						name:'商城开发',
						url: '/pages/shop/shop',
						type: true
					},
					{
						name:'百度小程序',
						url: '/pages/baidu/baidu',
						type: false
					},
					{
						name:'直销系统',
						url: '/pages/sell/sell',
						type: false
					},
					{
						name:'微信小程序',
						url: '/pages/wx/wx',
						type: false
					},
					{
						name:'关于我们',
						url: '/pages/relate/relate',
						type: false
					},
					{
						name:'联系我们',
						url: '/pages/concact/concact',
						type: false
					},
				],
			}
		},
		methods: {
			// 控制导航nav的显示或者隐藏
			handleListShow() {
				this.isListShow = !this.isListShow
			},
			// 实现页面的跳转
			handleType(options) {
				this.isListShow = false
				if(!options.type) {
					uni.navigateTo({
						url:options.url
					})
				}
				else {
					uni.switchTab({
						url:options.url
					})
				}	
			}
		}
	}
</script>

<style scoped>
	.header-box {
		display: flex;
		align-items: center;
		line-height: 120rpx;
		background: #242A37;
		padding-right: 18rpx;
		position: relative;
		justify-content: space-between;
	}
	.header-box image {
		width: 260rpx;
		height: 80rpx;
	}
	.header-box .icon-menu-two {
		color: #fff;
	}
	.select-box {
		position: absolute;
		right: 0;
		top: 120rpx;
	}
	.select-item {
		background: #242A37;
		line-height: 50rpx;
		font-size: 28rpx;
		color: #fff;
		box-sizing: border-box;
		border-bottom: 1px solid #fff;
		padding: 0 24rpx;
		text-align: center;
		z-index: 100;
	}
</style>
