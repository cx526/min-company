<template>
	<view>
		<view class="address-box">
			<view class="address-title">佛山市顺德区谷智精源软件开发有限公司</view>
			<view class="address-context">
				<view class="address-img">
					<image src="/static/images/loginBanner.jpg"></image>
				</view>
				<view class="address-way">
					<view>地址：广东省佛山市顺德区文海西路龙光尚街1座1725</view>
					<view>电话：0757-28983075 13480711960</view>
					<view>客服：1960669977</view>
					<view>邮箱：server@086soft.com</view>
					<view>网址：www.086soft.com www.086soft.cn</view>
				</view>
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
	.address-box {
		box-sizing: border-box;
		.address-title {
			box-sizing: border-box;
			line-height: 50rpx;
			text-align: center;
			background: #242A38;
			font-size: 28rpx;
			color: #fff;
		}
		.address-context {
			box-sizing: border-box;
			padding: 36rpx 24rpx;
			display: flex;
			.address-img {
				box-sizing: border-box;
				width: 250rpx;
				height: 250rpx;
				image {
					width: 100%;
					height: 250rpx;
				}
			}
			.address-way {
				font-size: 24rpx;
				color: #333;
				box-sizing: border-box;
				padding-left: 12rpx;
				view {
					margin-bottom: 12rpx;
				}
			}
		}
	}
</style>
