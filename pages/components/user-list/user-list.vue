<template>
	<view>
		<view class="user-list">
			<view class="list-box">
				<block v-for="(item,index) in list" :key="index">
					<view class="list-item">
						<view class="list-left " :class="item.icon"></view>
						<view class="list-right" hover-class="clickActive">
							<view>{{item.text}}</view>
							<view class="icon iconfont icon-left"></view>
						</view>
					</view>
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
		},
		props: {
			list: {
				type: Array
			}
		}
	}
</script>

<style lang="scss">
	.user-list {
		box-sizing: border-box;
		background: #F7F7F8;
		.list-box {
			box-sizing: border-box;
			.list-item {
				box-sizing: border-box;
				display: flex;
				align-items: center;
				justify-content: space-between;
				background: #fff;
				.list-left {
					font-size: 42rpx;
					color: #333;
					margin-left: 20rpx;
				}
				.list-right {
					flex: 1;
					box-sizing: border-box;
					margin-left: 24rpx;
					padding: 20rpx 20rpx 20rpx 16rpx;
					display: flex;
					justify-content: space-between;
					align-items: center;
					view:first-child {
						color: #333;
						font-size: 32rpx;
					}
					view:last-child {
						color: #999;
						font-size: 42rpx;
					}
				}	
			}
			.list-item:nth-child(2n-1) {
				.list-right {
					border-bottom: 1px solid #ccc;
				}
			}
			
			.list-item:nth-child(2n) {
				margin-bottom: 24rpx;
			}
		}
	}
	.clickActive {
		background: #f7f7f7 !important;
	}
</style>
