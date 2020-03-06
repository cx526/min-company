<template>
	<view>
		<Header></Header>
		<UserInfo></UserInfo>
		<UserMessage></UserMessage>
		<UserRecommend></UserRecommend>
		<UserList :list="list  "></UserList>
		
	</view>
</template>

<script>
	import Header from '../common/header/header'
	import UserInfo from '../components/user-info/user-info'
	import UserMessage from '../components/user-message/user-message'
	import UserRecommend from '../components/user-recommend/user-recommend'
	import UserList from '../components/user-list/user-list'
	export default {
		data() {
			return {
				list:[
					{
						icon:'icon iconfont icon-tongzhi',
						text:'平台公告'
					},
					{
						icon:'icon iconfont icon-xiaoxi--copy',
						text:'服务中心'
					},
					{
						icon:'icon iconfont icon-EPCzuodaohangtubiao-',
						text:'工单管理'
					},
					{
						icon:'icon iconfont icon-xiangmu',
						text:'我的项目'
					},
					{
						icon:'icon iconfont icon-tiwen',
						text:'建议反馈'
					},
					{
						icon:'icon iconfont icon-shezhi',
						text:'用户设置'
					},
				]
			}
		},
		components: {
			Header,
			UserInfo,
			UserMessage,
			UserRecommend,
			UserList
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">

	
</style>
