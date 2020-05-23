<template>
	<view class="context">
		<uni-nav-bar left-icon="back" title="项目列表"></uni-nav-bar>
		<view class="buttonWrapper">
			<button class="button" @tap="">进行中</button>
			<button class="button" @tap="">未开始</button>
			<button class="button" @tap="">已完成</button>
		</view>
		<search class="search-block"></search>
		<view class="introWrapper">
			<projectIntro class="project-intro" :name="name1" :location="location1" :time="time1" :progress="progress1"></projectIntro>
			<projectIntro class="project-intro" :name="name1" :location="location1" :time="time1" :progress="progress1"></projectIntro>
		</view>
	</view>
</template>

<script>
	import uniNavBar from "../../components/uni-nav-bar/uni-nav-bar.vue"
	import search from "../../components/search/search.vue";
	import projectIntro from "../../components/projectIntro/projectIntro.vue";
	export default {
		data() {
			return {
				name1: '安徽',
				location1: '合肥',
				time1: '2020年02月02日',
				progress1: '进行中'
			};
		},
		components: {
			uniNavBar,
			search,
			projectIntro
		},
		methods: {
			goBack: function() {
				uni.navigateTo({
					url: ''
				})
			}
		}
	};
</script>

<style>
	.context {
		display: flex;
		width: 100%;
		background-color: #ffffff;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.search-block {
		width: 90%;
	}

	/* 按钮框 */
	.buttonWrapper {
		display: flex;
		flex-direction: row;
		justify-content: center;
		height: 30px;
		width: 90%;
		margin-top: 10px;
	}

	.button {
		display: flex;
		height: 100%;
		width: 33.3%;
		font-size: 16px;
		justify-content: center;
		align-items: center;
		background-color: #fff;
		border: 1px solid #000000;
		border-radius: 0px;
	}

	.button::after {
		border: none;
	}

	/* 任务简介栏 */
	.introWrapper {
		margin-top: 5px;
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.project-intro {
		width: 100%;
		height: 100%;
	}
</style>
