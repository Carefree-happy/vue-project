<template>
	<li>
		<label>
			<!-- 如下代码也能使用，不太建议使用 -->
			<!-- <input type="checkbox" v-model="todo.done"/> -->
			<input type="checkbox" :checked="todo.done" @change="handleChecked(todo.id)"/>
			<span>{{todo.title}}</span>
		</label>
		<button class="btn btn-danger">删除</button>
	</li>
</template>

<script>
	export default {
		name:'MyItem',
		props:['todo', 'checkTodo'],
		mounted() {
			console.log(this.todo)
		},
		methods: {
			handleChecked(id) {
				this.checkTodo(id);
			}
		},
	}
</script>

<style scoped>
	/*item*/
	li {
		list-style: none;
		height: 36px;
		line-height: 36px;
		padding: 0 5px;
		border-bottom: 1px solid #ddd;
	}

	li label {
		cursor: pointer;
	}

	li label li input {
		vertical-align: middle;
		margin-right: 6px;
		position: relative;
		top: -1px;
	}

	li button {
		float: right;
		display: none;
		margin-top: 3px;
	}

	li:before {
		content: initial;
	}

	li:last-child {
		border-bottom: none;
	}

	li:hover{
		background-color: #ddd;
	}
	
	li:hover button{
		display: block;
	}
</style>