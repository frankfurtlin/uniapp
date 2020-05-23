<template>
	<view>
		<uni-nav-bar left-icon="back" title="成员详情" @clickLeft="back"></uni-nav-bar>
		<view class="memberInfo">
			<view class="memberInfoItem">
				<image style="width: 32px; height: 32px; background-color: #eeeeee;" :src='src' ></image>{{name}}
			</view>
			<view class="memberInfoItem">{{mobile}}</view>
			<view class="memberInfoItem">{{work}}</view>
		</view>
	</view>
</template>

<script>
	import uniNavBar from "../../components/uni-nav-bar/uni-nav-bar.vue";
	export default {
		components: {
			uniNavBar
		},
		data() {
			return {
				name: '张三',
				mobile: '13013445678',
				work: 'XX项目负责人',
				src: '../../static/head.png'
			};
		},
		methods: {
			back: function() {
				uni.navigateBack({
					url: './member/member'
				})	
			}
		}
	}
</script>

<style>
	.memberInfo {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-end;
	}

	.memberInfoItem {
		margin-top: 8px;
		padding-bottom: 6px;
		font-size: 16px;
		width: 95%;
		border-bottom: 1px solid #BBBBBB;
	}
</style>
