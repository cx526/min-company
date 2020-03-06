<template>
	<view>
		<view class="user-box">
			<Title title="谷智用户"></Title>
			<view class="user-list">
				<block v-for="(item,index) in 8" :key="index">
					<view class="user-item"></view>
				</block>
			</view>
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
		},
	}
</script>

<style lang="scss">
	.user-box {
		box-sizing: border-box;
		padding: 24rpx 16rpx 48rpx 16rpx;
		background: #242A38;
		margin-top: 24rpx;
		.user-list {
			box-sizing: border-box;
			display: flex;
			flex-wrap: wrap;
			margin-top: 24rpx;
			.user-item {
				box-sizing: border-box;
				margin-right: 16rpx;
				margin-bottom: 16rpx;
				height: 160rpx;
				width: calc(25% - 12rpx);
				background: #ccc;
			}
			.user-item:nth-child(4n) {
				margin-right: 0;
			}
		}
	}


</style>
