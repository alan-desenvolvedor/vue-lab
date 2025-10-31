<template>
  <div id="app">
    <input v-focus v-model="name" placeholder="Digite algo" />
    <p v-if="name">Você digitou: {{ name }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: ''
    }
  },
  directives: {
    focus: {
      mounted(el) {
        el.focus()
      }
    }
  }
}
</script>
