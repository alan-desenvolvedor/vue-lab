<template>
  <div id="app">

    <h1>{{ message }}</h1>

    <p>Contador: {{ counter }}</p>
    <button @click="incrementCounter">Aumentar</button>
    <button @click="resetCounter">Zerar</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      message: 'Conteúdo da variavel mensagem!',
      counter: 0
    }
  },
  methods: {
    incrementCounter() {
      this.counter++
    },
    resetCounter() {
      this.counter = 0
    }
  }
}
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button {
  margin: 5px;
  padding: 8px 16px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
button:hover {
  background-color: #2a8f68;
}
</style>
