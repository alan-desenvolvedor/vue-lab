<template>
  <div>
    <h2>Exemplo Simples de Watchers</h2>

    <p>Count: {{ count }}</p>
    <button @click="incrementCount">Incrementar</button>

    <p>Mensagem: {{ message }}</p>
    <button @click="changeMessage">Mudar Mensagem</button>

    <h3>Usuário:</h3>
    <p>Nome: {{ user.name }}</p>
    <button @click="changeUserName">Mudar Nome</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      message: 'Olá, Vue!',
      user: {
        name: 'Maria',
        age: 25
      }
    };
  },

  watch: {
    count(newVal, oldVal) {
      console.log(`Count mudou de ${oldVal} para ${newVal}`);
    },

    message(newVal, oldVal) {
      console.log(`Mensagem mudou de "${oldVal}" para "${newVal}"`);
    },

    user: {
      handler() {
        console.log('O objeto user foi alterado');
      },
      deep: true
    }
  },

  methods: {
    incrementCount() {
      this.count++;
    },
    changeMessage() {
      this.message = 'Nova mensagem!';
    },
    changeUserName() {
      this.user.name = 'João';
    }
  }
};
</script>
