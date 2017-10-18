<template>
	<div>
		<h3>接受兄弟组件传值</h3>
		<h4>{{author}}</h4>
	</div>
</template>

<script>	
	import store from '../vuex/store.js'
	export default{
		data(){
			return {
				mes:"初始值"
			}
		},
		computed: {
		  author () {
		  	return this.$store.state.author
		  }
		 }
	}
</script>

<style>
</style>