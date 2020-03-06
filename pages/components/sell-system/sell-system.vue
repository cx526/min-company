<template>
	<view>
		<view class="system-box">
			<scroll-view scroll-x="true">
				<view class="system-list">
					<block v-for="(item,index) in systemList" :key="index">
						<view class="system-item">
							<view :class="item.icon"></view>
							<view class="system-title">{{item.title}}</view>
							<view class="system-des">{{item.des}}</view>
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
			systemList: {
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
	.system-box {
		box-sizing: border-box;
		padding: 24rpx;
		 scroll-view {
			width: 100%;
			white-space: nowrap;
			box-sizing: border-box;
			white-space: nowrap;
			.system-list {
				white-space: nowrap;
				display: flex;
				.system-item {
					box-sizing: border-box;
					text-align: center;
					width: calc(50% - 14rpx);
					background: #F4FAFA;
					padding: 36rpx 0;
					margin-right: 16rpx;
					flex-shrink: 0;
					.icon {
						font-size: 80rpx;
						line-height: 80rpx;
						margin-bottom: 24rpx;
						color: #7F95BE;
					}
					.system-title {
						font-size: 28rpx;
						color: #333;
						white-space: nowrap;
						overflow: hidden;
						text-overflow: ellipsis;
					}
					.system-des {
						font-size: 24rpx;
						color: #666;
						margin-top: 12rpx;
						white-space: nowrap;
						overflow: hidden;
						text-overflow: ellipsis;
					}
				}
				.system-item:last-child {
					margin-right: 0;
				}
			}
		}
	}
</style>
