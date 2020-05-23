<template>
	<view>
		<uni-nav-bar left-icon="back" left-text="|" right-text="编辑" title="项目成员列表" @clickLeft="back" @clickRight="openEdit"></uni-nav-bar>
		<view>
			<t-table>
				<t-tr>
					<t-th>职务</t-th>
					<t-th>成员</t-th>
					<t-th>电话</t-th>
				</t-tr>
				<t-tr v-for="item in tableList" :key="item.id" class="tr">
					<t-td>{{ item.work }}</t-td>
					<t-td @tap="openInfo">{{ item.name }}</t-td>
					<t-td>{{ item.mobile }}</t-td>
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
						id: 0,
						work: '项目经理',
						name: '张三',
						mobile: 'XXXXXX'
					},
					{
						id: 1,
						work: '院内人士',
						name: '李四',
						mobile: 'XXXXXX'
					},
					{
						id: 2,
						work: '施工负责人',
						name: '王五',
						mobile: 'XXXXXX'
					},
					{
						id: 3,
						work: '施工管理员',
						name: '赵六',
						mobile: 'XXXXXX'
					}
				]
			};
		},
		methods: {
			back: function() {
				uni.navigateBack({
					url: '../info/info'
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
			openInfo: function() {
				uni.navigateTo({
					url: './memberInfo',
					success: res => {},
					fail: () => {},
					complete: () => {}
				})
			}
		}
	}
</script>

<style>
	.tr{
		height: 40px;
	}
</style>
