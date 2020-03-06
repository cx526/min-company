<template>
	<view>
		<view class="wx-type">
			<view class="type-box">
				<scroll-view scroll-x="true">
					<view class="type-list">
						<block v-for="(item,index) in typeList" :key="index">
							<view class="type-item">
								<view class="type-img">
									<text :class="item.icon"></text>
								</view>
								<view class="type-title">
									<view>{{item.title}}</view>
									<view>{{item.main}}</view>
								</view>
								<view class="type-des">
									{{item.des}}
								</view>
								<view class="type-btn">
									<button>立刻联系</button>
								</view>
							</view>
						</block>
					</view>
				</scroll-view>
			</view>
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

<style lang="scss">
	.wx-type {
		box-sizing: border-box;
		padding: 24rpx 0;
		background: #EDF7FF;
		.type-box {
			box-sizing: border-box;
			padding: 0 18rpx;
			.type-list {
				box-sizing: border-box;
				display: flex;
				.type-item {
					box-sizing: border-box;
					flex-shrink: 0;
					margin-right: 16rpx;
					width: calc(50% - 12rpx);
					background: #fff;
					padding: 0 24rpx;
					height: 600rpx;
					position: relative;
					.type-img {
						display: flex;
						align-items: center;
						justify-content: center;
						box-sizing: border-box;
						border: 1px solid #ccc;
						width: 90rpx;
						height: 90rpx;
						border-radius: 50%;
						position: relative;
						left: 50%;
						top: 12rpx;
						transform: translateX(-50%);
						padding: 0 20rpx;
						text {
							font-size: 36rpx;
							color: #666;
						}
					}
					.type-title {
						box-sizing: border-box;
						padding-top: 36rpx;
						view:first-child {
							font-size: 32rpx;
							color: #333;
						}
						view:last-child {
							font-size: 28rpx;
							color: #666;
							margin-top: 8rpx;
						}
					}
					.type-des {
						font-size: 24rpx;
						color: #666;
						margin-top: 12rpx;
					}
					.type-btn {
						box-sizing: border-box;
						position: absolute;
						bottom: 0;
						left: 24rpx;
						width: calc(100% - 48rpx);
						button {
							background: #fff;
							font-size: 24rpx;
							margin: 12rpx 0 24rpx 0;
							border: 1px solid #A3B3D6;
							color: #A3B3D6;
						}
					}
					
				}
				.type-item:last-child {
					margin-right: 0;
				}
			}
		}
	}
</style>
