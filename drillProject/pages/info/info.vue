<template>
	<view>
		<uni-nav-bar left-icon="back" left-text="|" right-text="编辑" title="项目详情" @clickLeft="back" @clickRight="openEdit"></uni-nav-bar>
		<view class="info">
			<view class="infoItem">项目名称<text class="infoText">{{name}}</text></view>
			<view class="infoItem">开工时间<text class="infoText">{{time}}</text></view>
			<view class="infoItem">项目地点<text class="infoText">{{location}}</text></view>
			<view class="infoItem">工点<text class="infoText">{{workPoint}}</text></view>
			<view class="infoItem">钻孔<text class="infoText">{{drill}}</text></view>
			<view class="infoItem">项目经理<text class="infoText">{{manager}}</text></view>
			<view class="infoItem" @tap="openMember">项目成员<text class="infoText">{{member}}</text></view>
			<view class="infoItem">项目日志<text class="infoText">{{log}}</text></view>
		</view>
		<view>
			<button type="primary" plain="true" class="ifoButton">导出任务书</button>
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
				name: '湖北定测  >',
				time: '2020/02/02  >',
				location: '合肥  >',
				workPoint: '0  >',
				drill: '15  >',
				manager: '张三  >',
				member: '3  >',
				log: '>'
			};
		},
		methods: {
			back: function() {
				uni.switchTab({
					url: '../index/index'
				})		
			},
			openEdit: function() {
				uni.navigateTo({
					url: './edit',
					success: res => {},
					fail: () => {},
					complete: () => {}
				})
			},
			openMember: function() {
				uni.navigateTo({
					url: '../member/member',
					success: res => {},
					fail: () => {},
					complete: () => {}
				})
			}
		}
	}
</script>

<style>
	.info {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-end;
	}

	.infoItem {
		margin-top: 8px;
		padding-bottom: 6px;
		font-size: 16px;
		width: 95%;
		border-bottom: 1px solid #BBBBBB;
	}

	.infoText {
		float: right;
		padding-right: 10px;
	}

	.ifoButton {
		margin-top: 60px;
		width: 40%;
	}
</style>
