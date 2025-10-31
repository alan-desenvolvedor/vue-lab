<template>
  <div id="app">
    <p v-if="estaVisivel">
      ✨ MENSAGEM SECRETA REVELADA! ✨
    </p>

    <button @click="alternar">
      {{ estaVisivel ? 'Esconder Mensagem' : 'Mostrar Mensagem' }}
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      estaVisivel: false 
    }
  },
  methods: {

    alternar() {
      this.estaVisivel = !this.estaVisivel; 
    }
  }
}
</script>

<style>
#app {
  text-align: center;
  padding: 20px;
}
button {
  padding: 10px 20px;
  cursor: pointer;
}
</style>