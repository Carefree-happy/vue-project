<template>
  <h1 @click="sayHello">我是APP组件</h1>
  <h2>姓名：{{ name }}</h2>
  <h2>年龄：{{ age }}</h2>
</template>
<script>
  export default {
    name: 'APP',
    setup() {
      // 数据
      let name = '张三'
      let age = 18

      // 方法
      function sayHello() {
        alert(`我叫${name},我今年${age}岁了，你好呀！`)
      }

      return {
        name,
        age,
        sayHello
      }
    }
  }
</script>