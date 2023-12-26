<template>
	<view>
		<button type="primary" @click="button1">选择微信聊天文件</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			button1()
			{
				wx.chooseMessageFile({
					count:50,
					type:'all',
					success: (data) => {
						console.log(data);
						console.log(data.tempFilePaths);
					},
					fail: (err) => {
						console.log(err);
					}
				})
			}
		}
	}
</script>

<style>

</style>
