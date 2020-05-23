<template>
	<view>
		<uni-nav-bar left-icon="back" left-text="|" title="编辑项目" @clickLeft="back"></uni-nav-bar>
		<view class="edit">
			<view class="editItem">*项目名称<input class="editInput"/></view>
			<view class="editItem">*项目地点<input class="editInput"/></view>
			<view class="editItem">*开工时间<input class="editInput"/></view>
			<view class="editItem">项目经理<text class="editText">{{manager}}</text></view>
			<view class="editItem">项目成员<text class="editText">{{member}}</text></view>
		</view>
		<view>
			<button type="primary" class="editButton">确定</button>
		</view>
	</view>
</template>

<script>
	import uniNavBar from "../../components/uni-nav-bar/uni-nav-bar.vue"
	export default {
		components: {
			uniNavBar
		},
		data() {
			return {
				manager: '张三  >',
				member: '3  >',
			};
		},
		methods:{
			back: function() {
				uni.navigateBack({
					url: './info'
				})	
			}
		}
	}
</script>

<style>
	.edit {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-end;
	}

	.editItem {
		margin-top: 8px;
		padding-bottom: 6px;
		font-size: 16px;
		width: 95%;
		border-bottom: 1px solid #BBBBBB;
	}

	.editText {
		float: right;
		padding-right: 10px;
	}

	.editButton {
		margin-top: 60px;
		width: 40%;
	}
	.editInput{
		float: right;
		margin: 2px;
		padding-right: 10px;
		border: 1px solid #888888;
	}
</style>
