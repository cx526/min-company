<template>
	<view>
		<view class="notice-box">
			<text class="icon iconfont icon-tongzhi"></text>
			<view>新闻公告：2019年春节放假通知</view>
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
	.notice-box {
		display: flex;
		line-height: 50rpx;
		background: #91949B;
		color: #fff;
		box-sizing: border-box;
		padding: 0 24rpx;
		text {
			font-size: 24rpx;
		}
		view {
			flex: 1;
			font-size: 24rpx;
			box-sizing: border-box;
			padding-left: 18rpx;
			overflow: hidden;
			white-space: nowrap;
			text-overflow: ellipsis;
		}
	}

</style>
