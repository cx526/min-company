<template>
	<view>
		<view class="superiority-box">
			<ShopTitle shopTitle="产品优势"></ShopTitle>
			<view class="superiority-context"></view>
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
	.superiority-context {
		box-sizing: border-box;
		height: 400rpx;
	}
</style>
