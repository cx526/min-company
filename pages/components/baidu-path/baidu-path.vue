<template>
	<view>
		<view class="path-box">
			<view class="path-title">接入流程</view>
			<scroll-view scroll-x="true">
				<view class="path-list">
					<block v-for="(item,index) in pathList" :key="index">
						<view class="path-item">
							<view class="path-img">
								<image :src="item.imgUrl"></image>
							</view>
								<view class="path-main">
									<text>{{item.textSpcial}}</text><text>{{item.textNormal}}</text>
								</view>
								<view class="path-des">{{item.des}}</view>
						</view>
						</block>
					</view>
			</scroll-view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			pathList: {
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
	.path-box {
		box-sizing: border-box;
		padding: 0 0 0 24rpx;
		.path-title {
			box-sizing: border-box;
			text-align: center;
			font-size: 32rpx;
			color: #333;
			font-weight: 700;
		}
		.path-list {
			box-sizing: border-box;
			padding: 24rpx 16rpx;
			display: flex;
			.path-item {
				box-sizing: border-box;
				flex-shrink: 0;
				margin-right: 16rpx;
				width: calc(50% - 12rpx);
				border: 1px solid #FAFAFA;
				position: relative;
				.path-img {
					position: absolute;
					left: 0;
					top: 0;
					width: 120rpx;
					height: 90rpx;
					image {
						width: 120rpx;
						height: 90rpx;
					}
				}
				.path-main {
					box-sizing: border-box;
					margin-top: 120rpx;
					padding: 0 24rpx;
					font-size: 28rpx;
					color: #333;
					font-weight: 700;
					text:first-child {
						display: inline-block;
						padding-bottom: 10rpx;
						border-bottom: 2px solid #333;
					}
				}
				.path-des {
					font-size: 24rpx;
					color: #666;
					padding: 24rpx;
				}
			}
		}
	}
</style>
