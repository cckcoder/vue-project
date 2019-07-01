<template>
  <div class="main">
		<ul>
			<li v-for="todo in todos" :key="todo.time" :style="{color: color}">
				{{todo.text}}
			</li>
		</ul>
  </div>
</template>

<script>

export default {
  name: 'main',
	filters: {
		capitalize (val) {
			return val.toUpperCase()
		}
	},
	data () {
		return {
			todos: [
				{
					text: 'Todo1',
					time: 1540352507,
					completed: true
				}
				,{
					text: 'Todo2',
					time: 1540352506,
					completed: true
				}
				,{
					text: 'Todo3',
					time: 1540352508,
					completed: true
				}
				,{
					text: 'Todo4',
					time: 1540352607,
					completed: false
				}
			],
			srcUrl: "www.google.co.th",
			color: 'red'
		}
	}
}
</script>

