<template>
  <div id="app">
    <h1 v-text="msg" ref="title"></h1>
    <button @click="showDOM">点我输出上面的元素</button>
		<School ref="sch"></School>
		<Student></Student>
  </div>
</template>

<script>
	//引入组件
	import School from './components/School'
	import Student from './components/Student'

export default {
  name: 'App',
  data() {
    return {
      msg: '欢迎学习Vue！'
    }
  },
  components: {
    School,
    Student
  },
  methods: {
    showDOM() {
      console.log(this.$refs.title)
      console.log(this.$refs.sch)
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
