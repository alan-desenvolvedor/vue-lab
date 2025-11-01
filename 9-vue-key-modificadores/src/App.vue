<template>
  <div>
    <input @keydown.enter="fazerAlgo" placeholder="Pressione Enter" />
    <input @keydown.tab="tabPressionado" placeholder="Pressione Tab" />
    <textarea @keydown.ctrl.enter="enviarFormulario" placeholder="Ctrl + Enter para Enviar"></textarea>
    <input @keydown.enter.prevent="naoEnviar" placeholder="Enter não envia" />
  </div>
</template>

<script>
export default {
  methods: {
    fazerAlgo() {
      alert('Você pressionou Enter!');
    },
    tabPressionado() {
      alert('Você pressionou Tab!');
    },
    enviarFormulario() {
      alert('Formulário enviado com Ctrl + Enter');
    },
    naoEnviar() {
      alert('Tecla Enter pressionada, mas a ação padrão foi impedida.');
    }
  }
};
</script>
