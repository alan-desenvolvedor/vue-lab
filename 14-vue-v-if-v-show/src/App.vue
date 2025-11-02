<template>
  <div>
    <p v-if="weather === 'sunny'">It's a sunny day!</p>
    <p v-else-if="weather === 'rainy'">It's raining!</p>
    <p v-else>Weather is unpredictable.</p>
    
    <p v-show="isVisible">I am visible!</p>

    <p v-for="number in numbers" :key="number" v-if="number % 2 === 0">{{ number }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      weather: 'sunny',
      isVisible: true,
      numbers: [1, 2, 3, 4, 5]
    };
  }
}
</script>