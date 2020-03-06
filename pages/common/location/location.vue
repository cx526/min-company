<template>
	<view>
		<view class="location">
			<text>首页->{{area}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		props:{
			area:{
				type:String
			}
		},
		methods: {
			
		}
	}
</script>

<style >
	.location {
		box-sizing: border-box;
		line-height: 80rpx;
		padding-left: 24rpx;
		border-bottom: 1px solid #EAEAEA;
	}
</style>
