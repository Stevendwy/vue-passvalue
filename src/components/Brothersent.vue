<template>
	<div>
		<button @click="senttobrother">发送兄弟之间传值</button>
	</div>
</template>

<script>
	import store from '../vuex/store.js'
	export default {
		methods:{
			senttobrother:function(){
				this.$store.commit('newAuthor',"form brother")
//				this.$store.state.author = this.inpuTxt
			}
		}
	}
</script>

<style>
</style>