<template name="projectIntro">
	<uni-swipe-action>
		<uni-swipe-action-item :options="options" @click="openInfo">
			<view class="projectIntro">
				<view class="header">{{name}}定测</view>
				<view class="textline">项目地点:{{location}}</view>
				<view class="textline">开工时间:{{time}}</view>
				<view class="textline">项目进度:{{progress}}</view>
			</view>
		</uni-swipe-action-item>
	</uni-swipe-action>
	<!-- <view class="projectIntro" @click="openInfo">
		<view class="header">{{name}}定测</view>
		<view class="textline">项目地点:{{location}}</view>
		<view class="textline">开工时间:{{time}}</view>
		<view class="textline">项目进度:{{progress}}</view>
	</view> -->
</template>

<script>
	import uniSwipeAction from '../uni-swipe-action/uni-swipe-action.vue';
	import uniSwipeActionItem from '../uni-swipe-action-item/uni-swipe-action-item.vue';
	export default {
		name: "projectIntro",
		data() {
			return {
				options: [{
					text: '删除',
					style: {
						backgroundColor: '#ff3a31'
					}
				}]
			};
		},
		// 此处定义传入的数据
		props: {
			name: {
				type: String,
				value: null
			},
			location: {
				type: String,
				value: null
			},
			time: {
				type: String,
				value: null
			},
			progress: {
				type: String,
				value: null
			}
		},
		methods: {
			openInfo: function() {
				uni.navigateTo({
					url: '../info/info',
					success: res => {},
					fail: () => {},
					complete: () => {}
				})
			}
		}
	};
</script>

<style>
	.projectIntro {
		height: 120px;
		width: 100%;
		border: 1px solid #e1e1e1;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.header {
		font-size: 18px;
		width: 85%;
	}

	.textline {
		margin-top: 8px;
		font-size: 12px;
		width: 85%;
	}
</style>
