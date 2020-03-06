<template>
	<view class="advantage-box">
		<Title bgColor="#D4D4D4" title="我们的优势" textColor="#363030"></Title>
		<view class="advantage-list">
			<block v-for="(item,index) in advantageList" :key="index">
				<view class="advantage-item" :class="{ advantageActive: currentIndex == index }" @click="handleAdvantage(index)">
					<view class="advantage-context">
						<view :class="item.icon"></view>
						<view>{{item.title}}</view>
					</view>
				</view>
			</block>
		</view>
	</view>
</template>

<script>
	import Title from '../index-title/index-title'
	export default {
		props: {
			advantageList: Array
		},
		components: {
			Title
		},
		data() {
			return {
				currentIndex: 0,
			};
		},
		methods:{
			// 点击添加类名
			handleAdvantage(index){
				console.log(index);
				this.currentIndex = index
			},
		
		}
	}
</script>

<style lang="scss">
	.advantage-box {
		box-sizing: border-box;
		padding-top: 24rpx;
		padding-bottom: 48rpx;
		.advantage-list {
			box-sizing: border-box;
			padding: 0 16rpx;
			display: flex;
			.advantage-item {
				flex: 1;
				box-sizing: border-box;
				border-right: 1px solid #fff;
				background: #DCDEDD;
				height: 160rpx;
				margin-top: 24rpx;
				font-size: 24rpx;
				line-height: 24rpx;
				text-align: center;
				color: #302E2F;
				.advantage-context {
					position: relative;
					top: 50%;
					transform: translateY(-50%);
				}
				.icon {
					font-size: 36rpx;
					line-height: 36rpx;
					margin-bottom: 16rpx;
				}
			}
			.advantage-item:last-child {
				border-right: 0;
			}
			.advantage-item.advantageActive {
				color: #fff;
				background: #242A38;
			}
		}
	}
	
	

	
	
</style>
