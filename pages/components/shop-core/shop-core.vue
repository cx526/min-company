<template>
	<view>
		<view class="core-box">
			<view class="core-title">
				<text>核心技术</text>
			</view>
			<view class="core-list">
				<block v-for="(item,index) in coreList" :key="index">
					<view class="core-item">
						<view class="core-topic"></view>
						<view class="core-title">{{item.title}}</view>
						<view class="core-des">{{item.des}}</view>
					</view>
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			coreList:{
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
	/* 核心技术 */
	.core-box {
		box-sizing: border-box;
		.core-title {
			font-size: 36rpx;
			line-height: 36rpx;
			color: #333;
			text-align: center;
			border-bottom: 1px solid #ccc;
			box-sizing: border-box;
			padding-bottom: 24rpx;
			font-weight: 700;
		}
		.core-list {
			box-sizing: border-box;
			padding: 18rpx 18rpx 36rpx 18rpx;
			display: flex;
			.core-item {
				box-sizing: border-box;
				flex: 1;
				margin-right: 18rpx;
				width: calc(33.33% - 9rpx);
				background: #ccc;
				text-align: center;
				view {
					box-sizing: border-box;
				}
				.core-topic {
					background: #333;
					height: 180rpx;
				}
				.core-title {
					line-height: 28rpx;
					font-size: 28rpx;
					margin-top: 12rpx;
					white-space: nowrap;
					overflow: hidden;
					text-overflow: ellipsis;
					color: #333;
				}
				.core-des {
					line-height: 25rpx;
					font-size: 24rpx;
					margin-bottom: 12rpx;
					color: #666;
				}
			}
			.core-item:last-child {
				margin-right: 0;
			}
		}
	}


	
	
	

</style>
