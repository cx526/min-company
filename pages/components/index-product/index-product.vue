<template>
	<view class="product-box">
		<Title bgColor="#D4D4D4" title="谷智产品" textColor="#363030"></Title>
		<view class="product-list">
			<block v-for="(item,index) in 4" :key="index">
				<view class="product-item"></view>
			</block>
		</view>
	</view>
</template>

<script>
	import Title from '../index-title/index-title'
	export default {
		data() {
			return {
				
			};
		},
		components: {
			Title
		}
	}
</script>

<style lang="scss">
	.product-box {
		box-sizing: border-box;
		padding: 24rpx 36rpx 48rpx 36rpx;
		.product-list {
			box-sizing: border-box;
			display: flex;
			margin-top: 24rpx;
			.product-item {
				flex: 1;
				box-sizing: border-box;
				background: #999999;
				margin-right: 36rpx;
				width: calc(25% - 24rpx);
				height: 130rpx;
				border-radius: 16rpx;
			}
			.product-item:last-child {
				margin-right: 0;
			}
		}
	}



</style>
