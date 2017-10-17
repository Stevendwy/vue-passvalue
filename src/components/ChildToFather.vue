<template>
	<div>
		<h2>子级给父级传值测试</h2>
		<button @click="sendMsg">子级给父级传值</button>
	</div>
</template>

<script>
	
	export default{
		methods:{
			sendMsg:function(){
				this.$emit("listenChildChange","this msg from child")
			}
		}
	}
</script>

<style>
</style>