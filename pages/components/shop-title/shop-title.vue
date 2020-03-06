<template>
	<view>
		<view class="related-title">{{shopTitle}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			} 
		},
		props: {
			shopTitle: {
				type: String
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
	.related-title {
		box-sizing: border-box;
		padding-left: 24rpx;
		line-height: 60rpx;
		font-size: 28rpx;
		color: #333;
		background: #CCCCCC;
	}
</style>
