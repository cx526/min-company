<template>
	<view>
		<view class="related-box">
			<ShopTitle shopTitle="相关功能"></ShopTitle>
			<view class="related-context"></view>
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
		components: {
			ShopTitle
		}
	}
</script>

<style lang="scss">
	.related-box {
		box-sizing: border-box;
		.related-context {
			box-sizing: border-box;
			height: 400rpx;
		}
	}
	
</style>
