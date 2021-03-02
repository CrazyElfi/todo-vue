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
  width: 550px;
  padding: 0;
  margin: 0 auto;
}

.input__wrapper {
  width: 100%;
  display: flex;
  justify-content: space-between;
}

#input {
  width: 430px;
  padding: 15px;
  border: 1px solid #2c3e50;
  font-size: 18px;
  outline: none;
}

#btn {
  //width: 70px;
  padding: 15px 10px;
  background-color: #2c3e50;
  outline: none;
  color: #fff;
  &:hover {
    background-color: #fff;
    color: #2c3e50;
  }
}

.btn-delete {
  background-color: #a71818;
  padding: 2px 5px;
  color: #fff;
  font-weight: bold;
  &:hover {
    background-color: #6a0707;
  }
}

#todos {
  width: 550px;
  padding: 0;
}
#todos li {
  text-align: left;
  list-style: none;
  border: 1px solid #ccc;
  padding: 5px 10px;
  margin-bottom: 10px;
  display: flex;
  justify-content: space-between;
}
</style>
