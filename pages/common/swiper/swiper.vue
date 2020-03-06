<template>
	<view>
		<view class="service-swiper">
			<swiper indicator-dots autoplay circular>
				<block v-for="(item,index) in serviceImg" :key="index">
					<swiper-item>
						<image :src="item" @click="productArticle(index)"></image>
					</swiper-item>
				</block>
			</swiper>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			serviceImg: {
				type: Array
			}
		},
		data() {
			return {
				
			};
		},
		methods:{
			productArticle(index) {
				this.$emit('productArticle',index)
			}
		}
	}
</script>

<style lang="scss">
	/* swiper */
	.service-swiper swiper {
		width: 100%;
		swiper-item {
			height: 300rpx;
			background: #ccc;
			image {
				width: 100%;
				height: 300rpx;
			}
		}
	}
	

</style>
