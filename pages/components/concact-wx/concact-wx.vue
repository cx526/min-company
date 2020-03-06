<template>
	<view>
		<view class="wx-box">
			<view class="wx-title">企业微信</view>
			<view class="wx-context">
				<block v-for="(item,index) in wxList" :key="index">
					<view class="wx-item">
						<view class="wx-img">
							<image src="/static/images/bannerBg.jpg"></image>
						</view>
						<view class="wx-text">{{item}}</view>
					</view>
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			wxList: {
				type: Array
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.wx-box {
		box-sizing: border-box;
		.wx-title {
			box-sizing: border-box;
			line-height: 50rpx;
			text-align: center;
			background: #242A38;
			font-size: 28rpx;
			color: #fff;
		}
		.wx-context {
			box-sizing: border-box;
			padding: 36rpx 24rpx;
			display: flex;
			.wx-item {
				box-sizing: border-box;
				margin-right: 24rpx;
				width: calc(33.33% - 16rpx);
				.wx-img {
					width: 100%;
					box-sizing: border-box;
					image {
						width: 100%;
						height: 200rpx;
					}
				}
				.wx-text {
					box-sizing: border-box;
					text-align: center;
					line-height: 28rpx;
					color: #333;
					font-size: 28rpx;
					margin-top: 12rpx;
				}
			}
			.wx-item:last-child {
				margin-right: 0;
			}
		}
	}
</style>
