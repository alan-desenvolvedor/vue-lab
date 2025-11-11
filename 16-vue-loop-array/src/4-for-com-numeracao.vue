<template>
  <div>
    <div v-for="n in 10" :key="n">{{ n }}</div>

    <div v-for="n in 10" :key="'zero-'+n">{{ n - 1 }}</div>

    <div v-for="n in reversedRange" :key="'rev-'+n">{{ n }}</div>

    <div v-for="n in customStep" :key="'step-'+n">{{ n }}</div>

    <div v-for="(n, index) in arrayForIndex" :key="'idx-'+index">{{ index }}: {{ n }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arrayForIndex: Array.from({ length: 10 }, (_, i) => i + 1)
    };
  },
  computed: {
    reversedRange() {
      return Array.from({ length: 10 }, (_, i) => i + 1).reverse();
    },
    customStep() {
      return Array.from({ length: Math.ceil(10 / 2) }, (_, i) => i * 2);
    }
  }
};
</script>