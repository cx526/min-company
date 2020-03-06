<template>
	<view>
		<view class="manage-box">
			<Title title="谷智管理"></Title>
			<image src="/static/images/manageBg.png"></image>
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
	.manage-box {
		background: #242A38;
		height: 240rpx;
		box-sizing: border-box;
		padding: 24rpx 36rpx 48rpx 36rpx;
		image {
			width: 100%;
			height: 120rpx;
		}
	}

</style>
