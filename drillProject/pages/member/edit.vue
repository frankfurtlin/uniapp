<template>
	<view>
		<uni-nav-bar left-icon="back" left-text="|" right-text="修改" title="成员列表" @clickLeft="back" @clickRight=""></uni-nav-bar>
		<view class="box">
			<t-table>
				<t-tr>
					<t-th>职务</t-th>
					<t-th>成员名</t-th>
					<t-th>增加</t-th>
					<t-th>删除</t-th>
				</t-tr>
				<t-tr v-for="item in tableList" :key="item.work">
					<t-td>{{ item.work }}</t-td>
					<t-td>{{ item.name }}</t-td>
					<t-td>+</t-td>
					<t-td>-</t-td>
				</t-tr>
			</t-table>
		</view>

	</view>
</template>

<script>
	import uniNavBar from "../../components/uni-nav-bar/uni-nav-bar.vue";
	import tTable from '../../components/t-table/t-table.vue';
	import tTh from '../../components/t-table/t-th.vue';
	import tTr from '../../components/t-table/t-tr.vue';
	import tTd from '../../components/t-table/t-td.vue';
	export default {
		components: {
			uniNavBar,
			tTable,
			tTh,
			tTr,
			tTd
		},
		data() {
			return {
				tableList: [
					{
						work: '项目经理',
						name: '张三',
					},
					{
						work: '院内人士',
						name: '李四',
					},
					{
						work: '施工负责人',
						name: '王五',
					},
					{
						work: '施工管理员',
						name: '赵六',
					}
				]
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
	.box{
		
	}
</style>
