<template>
	<view>
		<view class="plan-box">
			<view class="plan-title">
				<view>共筑计划</view>
				<view>从经营流量到经营用户，尽享生态红利</view>
			</view>
			<scroll-view scroll-x="true">
				<view class="plan-list">
					<block v-for="(item,index) in planList" :key="index">
						<view class="plan-item">
							<view class="plan-main">
								<text>{{item.textSpcial}}</text><text>{{item.textNormal}}</text>
							</view>
							<view class="plan-des">{{item.des}}</view>		
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
			planList: {
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
	.plan-box {
		box-sizing: border-box;
		padding-bottom: 24rpx;
		.plan-title {
			box-sizing: border-box;
			padding-bottom: 24rpx;
			view:first-child {
				box-sizing: border-box;
				font-size: 32rpx;
				color: #333;
				font-weight: 700;
				text-align: center;
				margin-bottom: 10rpx;
			}
			view:last-child {
				box-sizing: border-box;
				font-size: 28rpx;
				color: #666;
				text-align: center;
			}
		}
		.plan-list {
			box-sizing: border-box;
			margin-top: 24rpx;
			padding: 0 18rpx;
			display: flex;
			.plan-item {
				box-sizing: border-box;
				flex-shrink: 0;
				width: 50%;
				text-align: center;
				height: 200rpx;
				.plan-main {
					font-size: 28rpx;
					color: #333;
					text:first-child {
						font-size: 32rpx;
						font-weight: 700;
					}
				}
				.plan-des {
					box-sizing: border-box;
					padding: 0 24rpx;
					font-size: 24rpx;
					text-align: center;
					color: #666;
				}
			}
		}
	}
</style>
