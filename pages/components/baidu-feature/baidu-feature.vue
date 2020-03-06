<template>
	<view>
		<view class="feature-box">
			<view class="feature-title">
				<view>特色能力</view>
				<view>提供完整的解决方案，助力精准高效获聚用户</view>
			</view>
			<scroll-view scroll-x="true">
				<view class="feature-list">
					<block v-for="(item,index) in featureList" :key="index">
						<view class="feature-item">
							<view class="feature-img">
								<image :src="item.imgUrl"></image>
							</view>
							<view class="feature-context">
								<view>{{item.title}}</view>
								<view>{{item.des}}</view>
								<view>{{item.context}}</view>
							</view>
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
			featureList: {
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
	.feature-box {
		box-sizing: border-box;
		padding: 24rpx 0;
		.feature-title {
			box-sizing: border-box;
			view:nth-child(1) {
				text-align: center;
				font-size: 32rpx;
				font-weight: 700;
				line-height: 32rpx;
				color: #333;
			}
			view:nth-child(2) {
				text-align: center;
				font-size: 28rpx;
				line-height: 28rpx;
				color: #666;
				margin-top: 18rpx;
			}
		}
		.feature-list {
			box-sizing: border-box;
			display: flex;
			flex-wrap: nowrap;
			margin-top: 24rpx;
			.feature-item {
				box-sizing: border-box;
				width: 50%;
				text-align: center;
				flex-shrink: 0;
				.feature-img {
					box-sizing: border-box;
					image {
						width: 90rpx;
						height: 90rpx;
					}
				}
				.feature-context {
					text-align: center;
					box-sizing: border-box;
					height: 120rpx;
					view:nth-child(1) {
						font-size: 32rpx;
						line-height: 32rpx;
						font-weight: 700;
						box-sizing: border-box;
						color: #333;
					}
					view:nth-child(2) {
						font-size: 28rpx;
						line-height: 28rpx;
						box-sizing: border-box;
						color: #666;
						margin-top: 8rpx;
					}
					view:nth-child(3) {
						font-size: 28rpx;
						line-height: 28rpx;
						box-sizing: border-box;
						color: #666;
					}
				}
			}
		}
	}
</style>
