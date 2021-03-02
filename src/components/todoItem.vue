<template>
  <li>
    <!--    here need checkbox-->

    {{ todo.id }} {{ todo.text }}
    <button class="btn-delete" @click="$emit('remove', todo.id)">x</button>
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
