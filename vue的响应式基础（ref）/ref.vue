<template>
  <div>
    //因为count.value++了 所以这里会显示1 初始化是0
	  0：{{count}}
  </div>
</template>


<script setup>
	// 首先引入ref
	import { ref } from "vue";
	const count = ref(0)
	
	console.log(count)			//value:0
	console.log(count.value) 	//0
	count.value++ 
	console.log(count.value)	//1
	
</script>
<!-- 
 另外一直写法
 <script>
 	import { ref } from "vue";
 	
 	export default{
 		// setup是一个特殊的钩子
 		setup() {
 			const sount = ref(0)
 		}
 		// 暴露给模板 {{count}}
 		return{
 			count
 		}
 	}
 </script>
 -->
