<template>
	<view>
		<view class="info-box">
			<view class="info-list">
				<view class="info-left">
					<view class="info-img">
						<image src="/static/images/bannerBg.jpg"></image>
					</view>
					<view class="info-msg">
						<view>A先生</view>
						<view>1224</view>
					</view>
					<view class="icon iconfont icon-xinfeng"></view>
				</view>
				<view class="info-right icon iconfont icon-left"></view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.info-box {
		box-sizing: border-box;
		padding: 24rpx 12rpx;
		border-bottom: 1px solid #ccc;
		background: #F7F7F8;
		.info-list {
			box-sizing: border-box;
			display: flex;
			justify-content: space-between;
			align-items: center;
			.info-left {
				flex: 1;
				display: flex;
				align-items: center;
				.info-img {
					box-sizing: border-box;
					margin-right: 24rpx;
					image {
						width: 120rpx;
						height: 120rpx;
						border-radius: 50%;
					}
				}
				.info-msg {
					color: #333;
					font-size: 28rpx;
					line-height: 32rpx;
					box-sizing: border-box;
					margin-right: 24rpx;
				}
				.icon-xinfeng {
					font-size: 42rpx;
					color: #333;
				}
			}
			.info-right {
				font-size: 42rpx;
				color: #999999;
				font-weight: 700;
			}
		}
	}
</style>
