<template>
	<view>
		<view class="sell-service">
			<view class="service-title">
				<view>增值服务</view>
				<view>商创网络多年的经验，为客户解决多种增值服务，全方位提供360º解决方案</view>
			</view>
			<scroll-view scroll-x="true">
				<view class="service-list">
					<block v-for="(item,index) in serviceList" :key="index">
						<view class="service-item">
							<view class="item-top">
								<view :class="item.icon"></view>
								<view class="item-title">{{item.title}}</view>
							</view>
							<view class="item-bottom">
								<block v-for="(list,index) in item.list" :key="index">
									<view class="item-des">
										<view>{{list.main}}</view>
										<view>{{list.des}}</view>
									</view>
								</block>
								<view class="item-btn">
									<button>了解更多</button>
								</view>
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
			serviceList: {
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
	.sell-service {
		box-sizing: border-box;
		padding: 24rpx;
		.service-title {
			text-align: center;
			margin-bottom: 36rpx;
			view:nth-child(1) {
				font-size: 32rpx;
				line-height: 32rpx;
				color: #333;
			}
			view:nth-child(2) {
				font-size: 24rpx;
				line-height: 24rpx;
				color: #666;
				margin-top: 24rpx;
			}
		}
		.service-list {
			box-sizing: border-box;
			display: flex;
			flex-wrap: nowrap;
			.service-item {
				box-sizing: border-box;
				flex-shrink: 0;
				margin-right: 10rpx;
				width: calc(50% - 2.5rpx);
				box-shadow: 1px 1px 10rpx #ccc inset;
				.item-top {
					box-sizing: border-box;
					background: #FF886A;
					padding: 32rpx 0;
					.icon {
						font-size: 40rpx;
						line-height: 40rpx;
						color: #fff;
						text-align: center;
						margin-bottom: 24rpx;
					}
					.item-title {
						font-size: 32rpx;
						line-height: 32rpx;
						color: #fff;
						text-align: center;
					}
				}
				.item-bottom {
					box-sizing: border-box;
					padding: 24rpx 12rpx;
					.item-des {
						box-sizing: border-box;
						margin-bottom: 24rpx;
						view:nth-child(1) {
							font-size: 28rpx;
							line-height: 28rpx;
							color: #333;
							white-space: nowrap;
							overflow: hidden;
							text-overflow: ellipsis;
						}
						view:nth-child(2) {
							font-size: 24rpx;
							line-height: 24rpx;
							color: #666;
							margin-top: 12rpx;
							white-space: nowrap;
							overflow: hidden;
							text-overflow: ellipsis;
						}
					}
					.item-btn {
						box-sizing: border-box;
						button {
							// padding: 24rpx 18rpx;
							width: 70%;
							font-size: 28rpx;
							background: #fff;
							border: 1px solid #FF886A;
							color: #FF886A;
						}
					}
				}
			}
			.service-item:last-child {
				margin-right: 0;
			}
		}
	}
</style>
