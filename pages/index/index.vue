<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<button type="primary" @click = "login()">去登录</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello666'
			}
		},
		onLoad() {

		},
		methods: {
			login() {
			uni.navigateTo({
				url: '/pages/login/login',
				success: () => {
				setTimeout(() => {
					uni.showToast({
					title: '成功了',
					icon: 'none',    // 如果要纯文本，不要icon，将值设为'none'
					duration: 2000    // 持续时间为2秒
					})
				}, 100); // 延迟显示弹窗，单位为毫秒
				}
			})
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
