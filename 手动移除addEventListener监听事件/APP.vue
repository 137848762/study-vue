<template>
	<div ref="myElement">点击我</div>
</template>
<script>
	export default{
		mounted() {
			// 在组件挂载时添加监听事件
			this.$refs.myElement.addEventListener('click',this.handleClick);
			console.log("1");
		},
		beforeDestroy() {
			// 在组件销毁前移除监听事件
			this.$refs.myElement.removeEventListener('click',this.handleClick);
			console.log("2");
		},
		methods:{
			handleClick(event){
				console.log("事件被点击了");
			}
		}
	}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
