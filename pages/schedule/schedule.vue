<template>
	<view>
		<view>
			<button @click = "to_deadlines_page">
				查看我的To-Do
			</button>
		</view>
		<view>
			<button @click = "to_ranking_page">
				查看排行榜
			</button>
		</view>
		<view class = "enclose calendar_page">
			<calendar/>
		</view>
	</view>
</template>

<script>
	import calendar from "../../components/calendar/calendartest.vue"
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			to_deadlines_page(e) {
				uni.navigateTo({
				            // url: 'test?id=1&name=uniapp'  c传递参数
					
				    url: "/pages/deadlines/deadlines"
				
				})
			},
			to_ranking_page(e) {
				uni.navigateTo({
					url: "/pages/ranking/ranking"
				})
			}
		},
		components: {
			calendar
		}
	}
</script>

<style>
	.enclose {
		position: fixed;
		bottom: var(--window-bottom, 0);
		/* justify-content: center; */
		width: 100%;
		
	}
	.calendar_page {
		display: block;
		/* position: fixed; */
		
		left: auto;
		right: auto;
		/* padding-bottom: 5px; */
		flex-direction: column;
		justify-content: center;
		/* bottom: var(--window-bottom, 0); */
		/* vertical-align: bottom; */
		
	}
</style>

 

 