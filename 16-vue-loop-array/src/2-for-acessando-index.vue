<template>
  <ul>
    <li v-for="(item, index) in filteredItems" :key="index" :class="{ 'even-item': index % 2 === 0 }">
      {{ index + 100 }}: {{ item }}
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      items: ['Apple', 'Banana', 'Cherry', 'Date', 'Elderberry']
    };
  },
  computed: {
    filteredItems() {
      return this.items.filter((item, index) => index % 2 === 0);
    }
  }
};
</script>

<style>
.even-item {
  background-color: #f2f2f2;
}
</style> 