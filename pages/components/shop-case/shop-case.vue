<template>
	<view>
		<ShopTitle shopTitle="相关案例"></ShopTitle>
		<view class="case-list">
			<block v-for="(item,index) in 9" :key="index">
				<view class="case-item"></view>
			</block>
		</view>
	</view>
</template>

<script>
	import ShopTitle from '../shop-title/shop-title'
	export default {
		data() {
			return {
				
			};
		},
		components:{
			ShopTitle
		}
	}
</script>

<style lang="scss">
	.case-list {
		box-sizing: border-box;
		padding: 18rpx;
		display: flex;
		flex-wrap: wrap;
		.case-item {
			box-sizing: border-box;
			margin-right: 12rpx;
			width: calc(33.33% - 8rpx);
			box-sizing: border-box;
			height: 180rpx;
			background: #ccc;
			margin-bottom: 12rpx;
			background: #333;
		}
		.case-item:nth-child(3n) {
			margin-right: 0;
		}
	}
	
	
</style>
