<template>
	<view>
		<view class="sell-type">
			<view class="sell-title">
				<view>直销系统六合一</view>
				<view>上百种制度灵活搭配</view>
			</view>
			<scroll-view scroll-x="true">
				<view class="sell-list">
					<block v-for="(item,index) in typeList" :key="index">
						<view class="sell-item">
							<view class="item-top" :style="{background: item.topBg}">
								<view class="sell-img" :style="{background: item.imgBg}">
									<text :class="item.icon"></text>
								</view>
								<view class="item-title">{{item.title}}</view>
							</view>
							<view class="item-bottom">
								<view class="item-des">
									{{item.des}}
								</view>
								<view class="item-btn" :style="{border: '1px solid '+item.topBg,color: item.topBg}">在线沟通</view>
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
			typeList: {
				type: Array
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss" scoped>
	.sell-type {
		box-sizing: border-box;
		padding: 24rpx;
		.sell-title {
			box-sizing: border-box;
			text-align: center;
			margin-bottom: 24rpx;
			view:nth-child(1) {
				font-size: 32rpx;
				line-height: 32rpx;
				color: #333;
			}
			view:nth-child(2) {
				font-size: 24rpx;
				line-height: 24rpx;
				color: #666;
				margin-top: 8rpx;
			}
		}
		scroll-view {
			width: 100%;
			.sell-list {
				box-sizing: border-box;
				display: flex;
				flex-wrap: nowrap;
				padding-top: 60rpx;
				.sell-item {
					box-sizing: border-box;
					margin-right: 16rpx;
					width: calc(50% - 16rpx);
					flex-shrink: 0;
					box-shadow: 1px 1px 3px #ccc inset;
					.item-top {
						height: 140rpx;
						position: relative;
						.sell-img {
							width: 120rpx;
							height: 120rpx;
							border-radius: 50%;
							display: flex;
							align-items: center;
							justify-content: center;
							position: absolute;
							left: 50%;
							transform: translateX(-50%);
							top: -60rpx;
							.icon {
								font-size: 60rpx;
								color: #fff;
							}
						}
						.item-title {
							text-align: center;
							color: #fff;
							position: relative;
							top: 70rpx;
							margin-bottom: 24rpx;
						}
					}
					.item-bottom {
						box-sizing: border-box;
						padding: 12rpx;
						font-size: 28rpx;
						color: #666;
						line-height: 32rpx;
						position: relative;
						height: 280rpx;
						.item-btn {
							box-sizing: border-box;
							padding: 18rpx 24rpx;
							text-align: center;
							font-size: 28rpx;
							border-radius: 36rpx;
							margin: 24rpx 0;
							width: 70%;
							margin-left: 15%;
							position: absolute;
							bottom: 24rpx
						}
					}
				}
			}
		}
	}
</style>
