<template>
  <div>
    <addTodo
      v-model="newTodoText"
    @keydown.enter="addNewTodo"
    @addTodo="addNewTodo"/>
    <ul id="todos"
        v-if="todos.length">
      <todoItem
        v-for="todo in todos"
        :key="todo.id"
        :todo="todo"
        @remove="removeTodo"/>
    </ul>
    <h4 v-else>
      No tasks! You can add first task.
    </h4>
  </div>
</template>

<script>
import todoItem from '@/components/todoItem.vue'
import addTodo from '@/components/addTodo'

let nextTodoId = 1

export default {
  name: 'todoList',
  components: {
    addTodo,
    todoItem
  },
  data: () => {
    return {
      newTodoText: '',
      todos: [
        {
          id: nextTodoId++,
          text: 'Learn Vue'
        },
        {
          id: nextTodoId++,
          text: 'Learn about single-file components'
        },
        {
          id: nextTodoId++,
          text: 'Fall in love'
        }
      ]
    }
  },
  methods: {
    addNewTodo () {
      const trimmedText = this.newTodoText.trim()
      if (trimmedText) {
        this.todos.push({
          id: nextTodoId++,
          text: trimmedText
        })
        this.newTodoText = ''
      }
    },
    removeTodo (idToRemove) {
      console.log('remove')
      this.todos = this.todos.filter(todo => {
        return todo.id !== idToRemove
      })
    }
  }
}

</script>
