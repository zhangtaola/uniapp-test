<template>
	<view>
		<zjy-easyinput errorMessage v-model="value" focus placeholder="请输入内容" @input="input"></zjy-easyinput>	
	</view>
</template>

<script>
	export default {
		//我这边修改了
		data() {
			return {
				value: '',
				password: '',
				placeholderStyle: "color:#2979FF;font-size:14px",
				styles: {
					color: '#2979FF',
					borderColor: '#2979FF'
				}
			}

		},
		onLoad() {},
		onReady() {},
		methods: {
			input(e) {
				console.log('输入内容：', e);
			},
			iconClick(type) {
				uni.showToast({
					title: `点击了${type==='prefix'?'左侧':'右侧'}的图标`,
					icon: 'none'
				})
			}
		}
	}
</script>

<style lang="scss">
	.uni-mt-5 {
		margin-top: 5px;
	}
</style>
