<template>
	<view>
		<view class="nav-box">
			<view class="nav-list">
				<block v-for="(item,index) in navList" :key="index">
					<view class="nav-item" @click="handleNav(index)">{{item}}</view>
				</block>
			</view>
			<view class="nav-context">
				<block v-for="(item,index) in navList" :key="index">
					<view v-show="currentIndex == index" class="animated fadeInRight">{{item}}</view>
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
				currentIndex: 0
			};
		},
		methods: {
			// 实现tab切换
			handleNav(index) {
				console.log(index);
				this.currentIndex = index
			}
		}
		
	}
</script>

<style lang="scss">
	// nav
	.nav-box {
		box-sizing: border-box;
		margin-top: 24rpx;
		padding: 0 12rpx;
		.nav-list {
			box-sizing: border-box;
			display: flex;
			line-height: 40rpx;
			text-align: center;
		}
			.nav-item {
				flex: 1;
				background: #ff0000;
				box-sizing: border-box;
				border-right: 1px solid #fff;
				font-size: 20rpx;
				color: #fff;
			}
			.nav-item:nth-child(1) {
				background: #342C2A;
			}
			.nav-item:nth-child(2) {
				background: #484443;
			}
			.nav-item:nth-child(3) {
				background: #5F5D5E;
			}
			.nav-item:nth-child(4) {
				background: #747474;
			}
			.nav-item:nth-child(5) {
				background: #8B8B8B;
			}
			.nav-item:nth-child(6) {
				background: #A1A1A1;
			}
		.nav-context {
			box-sizing: border-box;
			padding: 24rpx;
			view {
				font-size: 24rpx;
				color: #fff;
				background: #ccc;
				height: 250rpx;
			}
		}	
	}
</style>
