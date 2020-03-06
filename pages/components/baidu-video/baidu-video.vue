<template>
	<view>
		<video :src="videoSrc" class="multimedia"></video>
	</view>
</template>

<script>
	export default {
		props: {
			videoSrc: {
				type: String
			}
		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.multimedia {
		box-sizing: border-box;
		width: 100%;
		margin-top: 24rpx;
		
	}
</style>
