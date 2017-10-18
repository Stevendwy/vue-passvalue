<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld fromfather="send to child" />
    <HelloWorld :fromfather="sendToChild" />
    <ChildToFather @listenChildChange="showChildChange" />
    <Brothersent />
    <Brotherget />
    <!--<router-view/>-->
  </div>
</template>

<script>
	
import HelloWorld from './components/HelloWorld'
import ChildToFather from './components/ChildToFather'
import Brothersent from './components/Brothersent'
import Brotherget from './components/Brotherget'

export default {
  name: 'app',
  components:{
  	HelloWorld,
  	ChildToFather,
  	Brothersent,
  	Brotherget
  },
  data(){
  	return {
  		sendToChild:"变量 改变"
  	}
  },
  methods:{
  	showChildChange:function(data){
  		console.log(data)
  	}
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
