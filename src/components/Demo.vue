<template>
	<h4>{{person}}</h4>
	<h2 @click="city+=',,,'">姓名：{{city}}</h2>
	<h2>姓名：{{name}}</h2>
	<h2>年龄：{{age}}</h2>
	<h2>薪资：{{job.j1.salary}}K</h2>
	<button @click="name+='~'">修改姓名</button>
	<button @click="age++">增长年龄</button>
	<button @click="job.j1.salary++">涨薪</button>
</template>

<script>
	import {ref,reactive,toRef,toRefs} from 'vue'
	export default {
		name: 'DemoInfo',
		setup(){
			let city = ref('上饶');
			let school = reactive({
				class: '6班'
			})
			//数据
			let person = reactive({
				name:'张三',
				age:18,
				job:{
					j1:{
						salary:20
					}
				}
			})

			const class1 = school.class
			console.log('%%%',class1)

			// const class2 = toRef(school,'class')
			// console.log('####',class2)

			const x = toRefs(person)
			console.log('******',x)

			//返回一个对象（常用）
			return {
				city,
				person,
				name:toRef(school,'class1'),
				// age:toRef(person,'age'),
				// salary:toRef(person.job.j1,'salary'),
				...toRefs(person)
			}
		}
	}
</script>

