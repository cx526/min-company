<template>
	<view>
		<view class="type-box">
			<view class="type-list">
				<block v-for="(item,index) in typeList" :key="index">
					<view class="type-item">
						<view></view>
						<view>{{item}}</view>
					</view>
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			typeList: {
				type:	Array
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.type-box {
		box-sizing: border-box;
		padding: 36rpx 18rpx;
		.type-list {
			box-sizing: border-box;
			display: flex;
			.type-item {
				flex: 1;
				box-sizing: border-box;
				margin-right: 16rpx;
				text-align: center;
				width: calc(25% - 12rpx);
				font-size: 28rpx;
				color: #333;
				view:first-child {
						box-sizing: border-box;
						height: 160rpx;
						border: 1px solid #333;
					}
				view:last-child {
						margin-top: 12rpx;
					}
			}
			.type-item:last-child {
				margin-right: 0;
			}
		}
	}
	

	

</style>
