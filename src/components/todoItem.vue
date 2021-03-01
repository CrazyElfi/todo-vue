<template>
  <li>
      {{  todo.id }} {{ todo.text }}
  </li>
</template>

<script>

export default {
  name: 'todoItem',
  props: {
    todo: {
      type: Object,
      required: true
    }
  }
}

</script>
