<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		},
		onError: function(err) {
			// 这里只能捕获方法内的异常，不能捕获生命周期中的逻辑异常
			console.log('onError: ', err)
		},
		onThemeChange() {
			console.log('系统主题变化')
		},
		onUnhandledRejection (err) {
			console.log('---')
			console.log('onUnhandledRejection')
			console.log('---')
		}
	}
</script>

<style>
	/*每个页面公共css */
</style>
