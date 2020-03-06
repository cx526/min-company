<template>
	<view>
		<view class="nav-box">
			<view class="nav-list">
				<block v-for="(item,index) in navList" :key="index">
					<view class="nav-item">
						<view class="nav-context"></view>
						<view class="nav-title">{{item}}</view>
					</view>
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			navList: {
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
	.nav-box {
		box-sizing: border-box;
		padding: 0 24rpx;
		margin-top: 24rpx;
		.nav-list {
			box-sizing: border-box;
			display: flex;
			.nav-item {
				box-sizing: border-box;
				margin-right: 12rpx;
				width: calc(33.33% - 4rpx);
				.nav-context {
					box-sizing: border-box;
					width: 100%;
					height: 200rpx;
					background: #ccc;
				}
				.nav-title {
					line-height: 40rpx;
					background: #009B4D;
					text-align: center;
					color: #fff;
					margin-top: 12rpx;
					font-size: 24rpx;
				}
			}
			.nav-item:nth-child(3) {
				margin-right: 0;
			}
		}
	}
</style>
