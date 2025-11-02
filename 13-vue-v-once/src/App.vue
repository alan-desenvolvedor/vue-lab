<template>
  <div>
    <!-- Rendered every time -->
    <div>{{ message }}</div>

    <!-- Rendered only once -->
    <div v-once>{{ message }}</div>

    <!-- Conditional rendering -->
    <div v-if="showElement" v-once>{{ someData }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello, Vue!",
      someData: "I am static data",
      showElement: true,
    };
  },
};
</script>