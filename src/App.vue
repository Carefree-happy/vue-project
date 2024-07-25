<template>
  <h1 @click="sayHello">我是APP组件</h1>
  <h2>姓名：{{ name }}</h2>
  <h2>年龄：{{ age }}</h2>
  <h3>工作种类：{{job.type}}</h3>
	<h3>工作薪水：{{job.salary}}</h3>
  <button @click="changeInfo">修改信息</button>
</template>
<script>
import { ref } from 'vue'
  export default {
    name: 'APP',
    setup() {
      // 数据
      let name = ref('张三')
      let age = ref(18)
      let job = ref({
				type:'前端工程师',
				salary:'30K'
			})

      function changeInfo() {
        name.value = 'lisi'
        age.value = 28
        job.value.type = 'UI设计师'
				job.value.salary = '60K'
      }

      // 方法
      function sayHello() {
        alert(`我叫${name.value},我今年${age.value}岁了，你好呀！`)
      }

      return {
        name,
        age,
        job,
        sayHello,
        changeInfo
      }
    }
  }
</script>