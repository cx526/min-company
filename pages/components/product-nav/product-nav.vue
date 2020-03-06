<template>
	<view class="show-box"> 
		<view class="product-show">
			<block v-for="(item,index) in productText" :key="index">
				<view class="product-item">
					<view></view>
					<view>{{item}}</view>
				</view>
			</block>	
		</view>
		<view class="show-nav">
			<block v-for="(item,index) in nav" :key="index">
				<view :class="{navActive: navIndex == index}" @click="handleNav(index)">{{item}}</view>
			</block>
		</view>
		<!-- context -->
		<block v-for="(item,index) in nav" :key="index">
			<view class="show-context">
				<view class="show-cms animated fadeInRight" v-show="navIndex == index">{{item}}</view>
			</view>
		</block>
	</view>
</template>

<script>
	export default {
		props: {
			productText: {
				type: Array
			},
			nav: {
				type: Array
			}
		},
		data() {
			return {
				navIndex: 0
			};
		},
		methods:{
			handleNav(index) {
				this.navIndex = index
			}
		}
	}
</script>

<style lang="scss">
	.show-box {
		box-sizing: border-box;
		padding-top: 36rpx;
		.product-show {
			box-sizing: border-box;
			padding: 0 18rpx;
			display: flex;
			margin-bottom: 24rpx;
			.product-item {
				flex: 1;
				box-sizing: border-box;
				margin-right: 16rpx;
				height: 180rpx;
				width: calc(25% - 12rpx);
				text-align: center;
				view:first-child {
					height: 150rpx;
					width: 100%;
					background: #ccc;
					border-radius: 8rpx;
				}
				view:last-child {
					line-height: 30rpx;
					font-size: 24rpx;
					margin-top: 12rpx;
				}
			}
			.product-item:last-child {
				margin-right: 0;
			}
		}
	}
	/* nav */
	.show-nav {
		display: flex;
		box-sizing: border-box;
		view {
			flex: 1;
			box-sizing: border-box;
			line-height: 50rpx;
			font-size: 28rpx;
			color: #fff;
			text-align: center;
			background: #666666;
			border-right: 1px solid #fff;
		}
		view:last-child {
			border-right: 0;
		}
	}


	.navActive {
		background: #242A38 !important;
	}
	/* context */
	.show-context {
		box-sizing: border-box;
		view {
			height: 400rpx;
			background: #ccc;
			padding: 0 18rpx;
		}
	}

</style>
