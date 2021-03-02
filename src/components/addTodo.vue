<template>
  <div class="input__wrapper">
    <input id="input"
           type="text"
           :value="value"
           v-on="listeners"
           placeholder="add todo here ..."
           >
    <button id="btn">Add todo</button>
  </div>
</template>

<script>
export default {
  name: 'addTodo',
  props: {
    value: {
      type: String,
      default: ''
    }
  },
  computed: {
    listeners () {
      return {
        ...this.$listeners,
        input: event => this.$emit('input', event.target.value)
      }
    }
  }
}
</script>
