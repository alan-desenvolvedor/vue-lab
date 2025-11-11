<template>
  <div>
    <p>Texto original: {{ message }}</p>
    <p>Texto com “filtro”: {{ uppercaseMessage }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'olá vue'
    };
  },
  computed: {
    uppercaseMessage() {
      return this.message.toUpperCase();
    }
  }
};
</script>
