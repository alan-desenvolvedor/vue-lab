<template>
  <div>
    <p v-if="mostrarIf">Estou visível com v-if</p>
    <p v-else>Estou oculto com v-else</p>

    <p v-show="mostrarShow">
      Estou visível ou oculto, mas sempre presente no DOM com v-show.
    </p>

    <div v-cloak>
      Isto não será exibido até que a compilação do Vue esteja completa.
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mostrarIf: true,
      mostrarShow: true
    };
  }
};
</script>

<style>
[v-cloak] {
  display: none;
}
</style>
