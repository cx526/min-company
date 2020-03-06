<template>
	<view>
		<view class="wx-case">
			<view>相关案例</view>
				<view class="case-context">
					<block v-for="(item,index) in 9" :key="index">
						<view class="case-item"></view>
					</block>
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
	.wx-case {
		padding: 0 18rpx;
		margin-top: 24rpx;
		box-sizing: border-box;
		line-height: 60rpx;
		font-size: 28rpx;
		text-align: center;
		color: #fff;
		view:first-child {
			background: #009B4D;
		}
		.case-context {
			box-sizing: border-box;
			display: flex;
			flex-wrap: wrap;
			margin-top: 24rpx;
			.case-item {
				box-sizing: border-box;
				margin-right: 18rpx;
				margin-bottom: 24rpx;
				width: calc(33.33% - 12rpx);
				height: 160rpx;
				background: #ccc;
			}
			.case-item:nth-child(3n) {
				margin-right: 0;
			}
		}
	}
</style>
