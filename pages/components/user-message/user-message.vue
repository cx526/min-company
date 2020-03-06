<template>
	<view>
		<view class="message-box">
			<view class="message-list">
				<view class="list-left " :class="{active: currentIndex == 1}" @click="handleProject()">
					<view class="list-text">
						<view>项目管理</view>
						<view>查看项目进程序</view>
					</view>
					<view class="list-icon icon iconfont icon-EPCzuodaohangtubiao-"></view>
				</view>
				<view class="list-right " :class="{active: currentIndex == 0}" @click="handleOrder()">
					<view class="list-text">
						<view>订单管理</view>
						<view>查看订单信息</view>
					</view>
					<view class="list-icon icon iconfont icon-EPCzuodaohangtubiao-"></view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				currentIndex: 0
			};
		},
		methods: {
			handleProject() {
				this.currentIndex = 0
			},
			handleOrder() {
				this.currentIndex = 1
			}
		}
	}
</script>

<style lang="scss">
	.message-box {
		box-sizing: border-box;
		padding: 36rpx 20rpx;
		border-bottom: 1px solid #ccc;
		background: #F7F7F8;
		.message-list {
			box-sizing: border-box;
			display: flex;
			.list-left,	
			.list-right {
				flex: 1;
				display: flex;
				align-items: center;
				background: #FF6600;
				justify-content: space-between;
				box-sizing: border-box;
				margin-right: 18rpx;
				padding: 20rpx;
				.list-text {
					color: #fff;
					flex: 1;
					text-align: center;
					view:first-child {
						font-size: 38rpx;
					}
					view:last-child {
						font-size: 28rpx;
					}
				}
				.list-icon {
					font-size: 60rpx;
					color: #fff;
				}
			}
			.list-right {
				margin-right: 0;
				margin-left: 18rpx;
			}
			.list-left.active {
				background: #999999;
			}
			.list-right.active {
				background: #999999;
			}
		}
	}
</style>
