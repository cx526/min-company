<template>
	<view>
		<view class="sell-new">
			<view class="new-title">
				<view>新闻动态</view>
				<view>及时了解新闻，紧随最新直销状态</view>
			</view>
			<view class="new-des">
				<view>公司动态</view>
				<view>More+</view>
			</view>
			<view class="new-list">
				<block v-for="(item,index) in newList" :key="index">
					<view class="new-item">
						<view class="new-img">
							<image :src="item.imgUrl"></image>
						</view>
						<view>{{item.des}}</view>
					</view>
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			newList: {
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
	.sell-new {
		box-sizing: border-box;
		padding: 24rpx 12rpx;
		.new-title {
			box-sizing: border-box;
			text-align: center;
			view:nth-child(1) {
				font-size: 32rpx;
				line-height: 32rpx;
				color: #333;
			}
			view:nth-child(2) {
				font-size: 28rpx;
				line-height: 28rpx;
				color: #666;
				margin-top: 18rpx;
			}
		}
		.new-des {
			box-sizing: border-box;
			display: flex;
			justify-content: space-between;
			padding-bottom: 16rpx;
			border-bottom: 1px dashed #666;
			margin-top: 24rpx;
			view:nth-child(1) {
				font-size: 28rpx;
				line-height: 28rpx;
				color: #666;
			}
			view:nth-child(2) {
				font-size: 28rpx;
				line-height: 28rpx;
				background: #666;
				color: #fff;
			}
		}
		.new-list {
			box-sizing: border-box;
			display: flex;
			margin-top: 12rpx;
			.new-item {
				flex: 1;
				margin-right: 16rpx;
				width: calc(33.33% - 12rpx);
				.new-img {
					box-sizing: border-box;
					padding: 12rpx;
					border: 1px solid #ccc;
					height: 184rpx;
					image {
						width: 100%;
						height: 160rpx;
					}
				}
				view:nth-child(2) {
					white-space: nowrap;
					overflow: hidden;
					text-overflow: ellipsis;
					font-size: 24rpx;
					line-height: 24rpx;
					color: #666;
					text-align: center;
					margin-top: 8rpx;
				}
			}
			.new-item:last-child {
				margin-right: 0;
			}
		}
	}
</style>
