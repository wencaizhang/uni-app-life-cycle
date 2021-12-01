<template>
	<view>
		<p>demo1</p>
		<button @click="componentAVisible = !componentAVisible">显示/隐藏 componentA</button>
		<component-a v-if="componentAVisible"></component-a>
	</view>
</template>

<script>
	import componentA from "./componentA.vue"
	export default {
		components: { componentA },
		data() {
			return {
				componentAVisible: true,
			}
		},
		onTabItemTap (obj) {
			// console.log('onTabItemTap from demo1')
			// console.log(obj)
		},
		mounted () {
			
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
