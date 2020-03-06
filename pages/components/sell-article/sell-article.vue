<template>
	<view>
		<view class="sell-list">
			<view class="list-title">
				<view>行业新闻</view>
				<view>More+</view>
			</view>
			<view class="list-item">
				<block v-for="(item,index) in articleList" :key="index">
					<view class="item">
						<view>{{item.title}}</view>
						<view>{{item.time}}</view>
					</view>
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			articleList: {
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
	.sell-list {
		box-sizing: border-box;
		padding: 24rpx 12rpx;
		.list-title {
			font-size: 28rpx;
			line-height: 28rpx;
			box-sizing: border-box;
			padding-bottom: 12rpx;
			border-bottom: 1px dashed #ccc;
			display: flex;
			color: #666;
			justify-content: space-between;
			view:nth-child(2) {
				color: #fff;
				background: #666;
			}
		}
		.list-item {
			box-sizing: border-box;
			font-size: 24rpx;
			line-height: 24rpx;
			color: #333;
			.item {
				box-sizing: border-box;
				display: flex;
				margin-top: 20rpx;
				justify-content: space-between;
			}
		}
	}
</style>
