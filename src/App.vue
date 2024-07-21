<template>
  <div id="app">
    <button>点我输出上面的元素</button>
		<Student name="张三" sex="男" :age="12"></Student>
  </div>
</template>

<script>
	//引入组件
	import Student from './components/Student'

export default {
  name: 'App',
  data() {
    return {
      msg: '欢迎学习Vue！'
    }
  },
  components: {
    Student
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
