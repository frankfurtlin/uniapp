<template>
	<view>
		<view class="box">
			<view class="title">标段名称1</view>
			<text>\n</text>
			<t-table>
				<t-tr>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image><view>进程设备总数</view></t-td>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>工作设备数</t-td>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>在线设备数</t-td>
				</t-tr>
				<t-tr>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>完成孔数</t-td>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>完成米数</t-td>
					<t-td>···</t-td>
				</t-tr>
			</t-table>
		</view>
		<text>\n</text>
		<view class="box">
			<view class="title">标段名称2</view>
			<text>\n</text>
			<t-table>
				<t-tr>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>进程设备总数</t-td>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>工作设备数</t-td>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>在线设备数</t-td>
				</t-tr>
				<t-tr>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>完成孔数</t-td>
					<t-td><image style="width: 36px; height: 36px" src="../../static/image.png"></image>完成米数</t-td>
					<t-td>···</t-td>
				</t-tr>
			</t-table>
		</view>
	</view>
</template>

<script>
	import tTable from '@/components/t-table/t-table.vue';
	import tTh from '@/components/t-table/t-th.vue';
	import tTr from '@/components/t-table/t-tr.vue';
	import tTd from '@/components/t-table/t-td.vue';
	export default {
		components: {
			tTable,
			tTh,
			tTr,
			tTd
		},
		data() {
			return {
				title: 'Hello',
				tableList: [{
						id: 0,
						name: '张三',
						age: '19',
						hobby: '游泳'
					},
					{
						id: 1,
						name: '李四',
						age: '21',
						hobby: '绘画'
					},
					{
						id: 2,
						name: '王二',
						age: '29',
						hobby: '滑板'
					},
					{
						id: 3,
						name: '码字',
						age: '20',
						hobby: '蹦极'
					}
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>

</style>
