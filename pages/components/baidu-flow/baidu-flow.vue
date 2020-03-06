<template>
	<view>
		<view class="flow-box">
			<view class="flow-title">
				<view>流量支持</view>
				<view>提供完整的解决方案，助力精准高校获取用户</view>
			</view>
			<view class="flow-nav">
				<block v-for="(item,index) in navList" :key="index">
					<view @click="handleNav(index)">
						<text :class="index==navIndex?'active' : ''">{{item}}</text>
					</view>
				</block>
			</view>
			<view class="flow-context">
				<block v-for="(item,index) in navList" :key="index">
					<template v-if="index == navIndex">
						<view class="animated fadeInRight">{{item}}</view>
					</template>
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			navList: {
				type: Array
			}
		},
		data() {
			return {
				navIndex: 0,
			};
		},
		methods: {
			handleNav(index) {
				console.log(index);
				this.navIndex = index
			}
		}
	}
</script>

<style lang="scss">
	.flow-box {
		box-sizing: border-box;
		padding: 24rpx 0;
		.flow-title {
			box-sizing: border-box;
			margin-bottom: 24rpx;
			view:first-child {
				font-size: 32rpx;
				color: #333;
				text-align: center;
				margin-bottom: 10rpx;
				font-weight: 700;
			}
			view:last-child {
				font-size: 28rpx;
				color: #666;
				text-align: center;
			}
		}
		.flow-nav {
			box-sizing: border-box;
			display: flex;
			font-size: 28rpx;
			padding: 0 24rpx;
			border-bottom: 1px solid #ccc;
			view {
				box-sizing: border-box;
				flex: 1;
				text-align: center;
				text {
					display: inline-block;
					padding-bottom: 12rpx;
				}
				text.active {
					border-bottom: 2px solid #598AD3;
					color: #598AD3;
					font-weight: 700;
				}
			}
		}
		.flow-context {
			box-sizing: border-box;
			padding:36rpx 24rpx;
			font-size: 28rpx;
			color: #333;
			view {
				height: 240rpx;
				background: #ccc;
			}
		}
	}
</style>
