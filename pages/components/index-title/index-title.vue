<template>
	<view>
		<view class="advantage-title">
			<view class="line" :style="{background: bgColor}"></view>
			<view class="title" :style="{color: textColor}">{{title}}</view>
			<view class="line" :style="{background: bgColor}"></view>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			bgColor: {
				type: String,
				default: '#fff'
			},
			textColor: {
				type: String,
				default: '#fff'
			},
			title:{
				type: String,
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

<style scoped>
	.advantage-title {
		font-size: 36rpx;
		text-align: center;
		font-weight: 700;
		line-height: 40rpx;
		position: relative;
	}
	.advantage-title .line {
		height: 1px;
		width: 200rpx;
		position: absolute;
		left: 8%;
		top: 50%;
	}
	.advantage-title .line:last-child {
		left: 65%;
	}
</style>
