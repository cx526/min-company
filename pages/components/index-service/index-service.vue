<template>
	<view class="service-box">
		<Title bgColor="#D4D4D4" title="谷智服务" textColor="#363030"></Title>
		<view class="service-des">
			<view class="service-topic"></view>
			<view class="service-title">
				<view>二次开发，选服务</view>
				<view>就选谷智精源</view>
			</view>
		</view>
	</view>
</template>

<script>
	import Title from '../index-title/index-title'
	export default {
		data() {
			return {
				
			};
		},
		components: {
			Title
		}
	}
</script>

<style lang="scss">
	.service-box {
		box-sizing: border-box;
		padding-top: 24rpx;
		.service-des {
				box-sizing: border-box;
				margin: 24rpx auto 18rpx;
				padding: 36rpx;
				display: flex;
				background: #242A38;
				justify-content: space-between;
				.service-topic {
					width: 160rpx;
					height: 160rpx;
					background: #CCC;
				}
				.service-title {
					flex: 1;
					color: #fff;
					box-sizing: border-box;
					text-align: right;
					view:first-child {
						font-size: 40rpx;
						margin-top: 12rpx;
					}
					view:last-child {
							font-size: 52rpx;
							margin-top: 12rpx;
						}
				}
			}
	}
	


	
	
</style>
