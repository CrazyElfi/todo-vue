<template>
  <div id="app">
    <h2> {{ title }}</h2>
    <todoList/>
  </div>
</template>

<script>
import todoList from './components/todoList.vue'

export default {
  name: 'App',
  components: {
    todoList
  },
  data: function () {
    return {
      title: 'TodoList'
    }
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  font-size: 20px;
  color: #2c3e50;
  width: 400px;
  margin: 0 auto;
}

#input {
  width: 400px;
  padding: 15px;
  border: 1px solid #2c3e50;
  font-size: 18px;
}
#todos {
  width: 100%;
  padding: 0;
}
#todos li {
  width: 100%;
  text-align: left;
  list-style: none;
  border: 1px solid #ccc;
  padding: 5px 10px;
  margin-bottom: 10px;
}
</style>
