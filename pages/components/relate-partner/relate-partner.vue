<template>
	<view>
		<view class="partner-box">
			<view class="partner-title">
				<view>合作伙伴</view>
				<image src="/static/images/tagline-first.jpg"></image>
			</view>
			<view class="partner-list">
				<block v-for="(item,index) in 12" :key="index">
					<view class="partner-item"></view>
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
	// 合作伙伴
	.partner-box {
		box-sizing: border-box;
		.partner-title {
			box-sizing: border-box;
			padding: 0 20rpx;
			line-height: 50rpx;
			color: #fff;
			display: flex;
			align-items: center;
			justify-content: space-between;
			background: #8B8B8B;
			view {
				font-size: 24rpx;
			}
			image {
				max-width: 300rpx;
				flex: 1;
				height: 50rpx;
			}
		}
		.partner-list {
			box-sizing: border-box;
			padding: 24rpx 12rpx;
			display: flex;
			flex-wrap: wrap;
			.partner-item {
				box-sizing: border-box;
				margin-right: 18rpx;
				margin-bottom: 18rpx;
				width: calc(33.33% - 12rpx);
				height: 200rpx;
				background: #ccc;
			}
			.partner-item:nth-child(3n) {
				margin-right: 0;
			}
		}
	}
</style>
