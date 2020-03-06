<template>
	<view  class="dynamic-box" >	
		<view class="dynamic-list">
			<block v-for="(item,index) in articleList" :key="index">
				<view class="dynamic-item" hover-class="clickActive" @click="handelContext()">
					<view class="dynamic-img">
						<image :src="item.topic"></image>
					</view>
					<view class="dynamic-main">
						<view class="title">{{item.title}}</view>
						<view class="des">{{item.des}}</view>
						<view class="dynamic-icon">
							<view class="time">
								<text class="icon iconfont icon-clock"></text>
								<text>{{item.time}}</text>
							</view>
						<!-- 	<view class="wx">
								<text class="icon iconfont icon-weixindefuben" ></text>
								<text class="icon iconfont icon-xinlang" ></text>
							</view> -->
						</view>
					</view>
				</view>
			</block>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				articleList: [
					{
						topic: '/static/images/bannerBg.jpg',
						title: '文章主题',
						des: '文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明',
						time: '2020-02-20'
					},
					{
						topic: '/static/images/bannerBg.jpg',
						title: '文章主题',
						des: '文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明',
						time: '2020-02-20'
					},
					{
						topic: '/static/images/bannerBg.jpg',
						title: '文章主题',
						des: '文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明文章说明',
						time: '2020-02-20'
					},
				]
			};
		},
		components: {
			
		},
		methods: {
			// 跳转到内容页
			handelContext() {
				uni.navigateTo({
					url: '/pages/components/dynamic-context/dynamic-context'
				})
			}

		}
	}
</script>

<style lang="scss">
	.dynamic-box {
		box-sizing: border-box;
		padding: 24rpx 18rpx 0 18rpx;
		.dynamic-title view:first-child {
			font-size: 28rpx;
			color: #6E6E6E;
		}
		.dynamic-title view:last-child {
			font-size: 24rpx;
			color: #999;
			margin-top: 24rpx;
			white-space: nowrap;
			overflow: hidden;
			text-overflow: ellipsis;
		}
		.dynamic-des {
			margin-top: 36rpx;
			font-size: 28rpx;
			color: #6E6E6E;
			display: flex;
			justify-content: space-between;
			line-height: 28rpx;
		}
		.dynamic-des text:last-child {
			color: #FF8800;
		}
		.dynamic-list {
			box-sizing: border-box;
			margin-top: 24rpx;
			margin-bottom: 24rpx;
			.dynamic-item {
				box-sizing: border-box;
				display: flex;
				margin-bottom: 24rpx;
				.dynamic-img {
					width: 240rpx;
					height: 160rpx;
					image {
						width: 100%;
						height: 160rpx;
					}
				}
				.dynamic-main {
					box-sizing: border-box;
					flex: 1;
					padding: 0 18rpx;
					.title {
						font-size: 28rpx;
						line-height: 28rpx;
						color: #333;
						overflow: hidden;
						text-overflow: ellipsis;
						white-space: nowrap;
					}
					.des {
						font-size: 24rpx;
						color: #666;
						margin-top: 16rpx;
						overflow : hidden;
						text-overflow: ellipsis;
						display: -webkit-box;
						-webkit-line-clamp: 2;
						-webkit-box-orient: vertical;
					}
					.dynamic-icon {
						display: flex;
						font-size: 28rpx;
						align-content: center;
						margin-top: 16rpx;
						color: #666;
						.time {
							flex: 1;
						}
						.icon{
							margin-right: 16rpx;
						}
						.icon-weixindefuben {
							color: #789E6D;
						}
						.icon-xinlang {
							color: #B9494B;
							margin-right: 0;
						}
					}
				}
			}
		}
	}
	.clickActive {
		background: #f7f7f7 !important;
	}
</style>
