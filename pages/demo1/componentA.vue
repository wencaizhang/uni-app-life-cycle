<template>
<div>
	<h1 ref="title">{{ title }}</h1>
	<p>componentA</p>
</div>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello ComponentA'
			}
		},
		beforeCreate() {
			console.log('%c 🥪 beforeCreate: ', 'font-size:20px;background-color: #B03734;color:#fff;')
			console.log('访问 data: ', this.title)
			console.log('访问 methods: ', this.updateTitle)
			console.log(this.$refs.title)
			console.log('---------')
		},
		created() {
			console.log('%c 🥪 created: ', 'font-size:20px;background-color: #B03734;color:#fff;')
			console.log('访问 data: ', this.title)
			console.log('访问 methods: ', this.updateTitle)
			console.log(this.$refs.title)
			console.log('---------')
		},
		beforeMount() {
			console.log('%c 🥪 beforeMount: ', 'font-size:20px;background-color: #B03734;color:#fff;')
			console.log('访问 data: ', this.title)
			console.log('访问 methods: ', this.updateTitle)
			console.log(this.$refs.title)
			console.log('---------')
		},
		mounted () {
			console.log('%c 🥪 mounted: ', 'font-size:20px;background-color: #B03734;color:#fff;')
			console.log('访问 data: ', this.title)
			console.log('访问 methods: ', this.updateTitle)
			console.log(this.$refs.title)
			console.log('---------')
			setTimeout(() => {
				this.updateTitle()
			}, 2000)
		},
		beforeUpdate () {
			console.log('%c 🥪 beforeUpdate: ', 'font-size:20px;background-color: #B03734;color:#fff;')
			console.log('访问 data: ', this.title)
			console.log('访问 methods: ', this.updateTitle)
			console.log('---------')
		},
		updated () {
			console.log('%c 🥪 updated: ', 'font-size:20px;background-color: #B03734;color:#fff;')
			console.log('访问 data: ', this.title)
			console.log('访问 methods: ', this.updateTitle)
			console.log('---------')
		},
		beforeDestroy () {
			console.log('%c 🥪 beforeDestroy: ', 'font-size:20px;background-color: #B03734;color:#fff;')
			console.log('访问 data: ', this.title)
			console.log('访问 methods: ', this.updateTitle)
			console.log('---------')
		},
		destroyed () {
			console.log('%c 🥪 destroyed: ', 'font-size:20px;background-color: #B03734;color:#fff;')
			console.log('访问 data: ', this.title)
			console.log('访问 methods: ', this.updateTitle)
			console.log('---------')
		},
		methods: {
			updateTitle () {
				this.title = 'updated title: Hello ComponentA'
			}
		}
	}
</script>

