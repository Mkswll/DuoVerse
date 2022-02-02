<template>
	<view>
		<view class = "calendar_mod">
		    <uni-calendar 
		    :insert = "true"
			:date = "info.date"
		    :start-date="info.startDate"
		    :end-date="info.endDate"
		    @change="change"
		    />
			<view>
				<button class = "button_box" @click = "click_event">
					<view class = "add_tab">
						添加任务
					</view>
				</button>
			</view>
			
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: {
					
				}
			}
		},
		mounted() {
			this.$nextTick(() => {
				this.showCalendar = true
			})
			// TODO 模拟请求异步同步数据
			setTimeout(() => {
				this.info.date = getDate(new Date(),-30).fullDate
				this.info.startDate = getDate(new Date(),-60).fullDate
				this.info.endDate =  getDate(new Date(),30).fullDate
				this.info.selected = [
					
				]
			}, 2000)
		},
		methods: {
			change() {
				
			},
			click_event() {
				// this.num++;
			}
		}
	}
</script>

<style>
	.calendar_mod {
		padding: 10px;
	}
	.button_box {
		display: flex;
		background-color: #eef;
		justify-content: center;
		width: 100px;
		
		
	}
	.add_tab {
		display: flex;
		font-size: 15px;
		line-height: 30px;
		align-items: center;
		justify-content: center;
		
		/* background-color: #eef; */
		/* text-font: 20px, */
	}
</style>
