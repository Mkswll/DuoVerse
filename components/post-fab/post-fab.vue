<template>
	<view>
		<uni-fab
		    :pattern = "pattern"
			:content = "content"
		    :horizontal = "horizontal"
		    :vertical = "vertical"
			@trigger = "to_post_page"
		>
		</uni-fab>
	
	</view>
</template>

<script>
	export default {
		name: "post-fab",
		data() {
			return {
				horizontal: 'right',
				vertical: 'bottom',
				pattern: {
					color: '#7A7E83',
					backgroundColor: '#fff',
					selectedColor: '#007AFF',
					buttonColor: '#007AFF',
					iconColor: '#fff'
				},
				content: [{
					iconPath: '/static/user%20icon.png',
					// selectedIconPath: '/static/image-active.png',
					text: '发布',
					active: false
				},
				{
					iconPath: '/static/user%20icon.png',
					text: '鼓励箱',
					active: false
				}]
			}
		},
		methods: {
			to_post_page(e) {
				uni.navigateTo({
				            // url: 'test?id=1&name=uniapp'  c传递参数
					
				    url:"/pages/post/post"
				
				})
			},
			trigger(e) {
				this.content[e.index].active = !e.item.active
			}
		}
	}
</script>

<style>

</style>
