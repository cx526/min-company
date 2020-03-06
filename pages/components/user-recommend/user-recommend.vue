<template>
	<view>
		<view class="recommend-box">
			<view class="recommend-title">
				<view>谷智推荐</view>
				<view class="icon iconfont icon-chanpin1"></view>
			</view>
			<view class="recommend-list">
				<block v-for="(item,index) in 3" :key="index">
					<view class="recommend-item"></view>
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.recommend-box {
		box-sizing: border-box;
		background: #F7F7F8;
		.recommend-title {
			background: #fff;
			box-sizing: border-box;
			padding: 20rpx 24rpx;
			font-size: 32rpx;
			line-height: 32rpx;
			color: #333;
			display: flex;
			align-items: center;
			justify-content: space-between;
			view:first-child {
				flex: 1;
			}
			view:last-child {
				color: #999;
				font-size: 42rpx;
			}
		}
		.recommend-list {
			box-sizing: border-box;
			padding: 36rpx 24rpx;
			display: flex;
			.recommend-item {
				flex: 1;
				margin-right: 18rpx;
				width: calc(33.33% - 12rpx);
				box-sizing: border-box;
				height: 160rpx;
				border: 1px solid #333;
			}
		}
	}
</style>
