<template>
	<view>
		<view class="case-title">相关案例</view>
		<view class="case-list">
			<block v-for="(item,index) in 9" :key="index">
				<view class="case-item"></view>
			</block>
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
	.case-title {
		box-sizing: border-box;
		margin-bottom: 24rpx;
		text-align: center;
		color: #333;
		font-weight: 700;
		font-size: 32rpx;
	}
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
			border: 1px solid #ccc;
			margin-bottom: 12rpx;
		}
		.case-item:nth-child(3n) {
			margin-right: 0;
		}
	}
</style>
