<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<button @click="fn">reject</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {
			console.log('onLoad')
			// throw new Error('onLoad 出错啦')
			// this.fn()
		},
		mounted () {
			this.fn()
			// this.emitError()
		},
		onTabItemTap (obj) {
			console.log('onTabItemTap from index')
			console.log(obj)
		},
		methods: {
			emitError () {
				return a;
			},
			fn () {
				return new Promise((resolve, reject) => {
					setTimeout(() => {
						reject('onUnhandledRejection 测试')
					}, 2000)
				})
			}
		},
		
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
