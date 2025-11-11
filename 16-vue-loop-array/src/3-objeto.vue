<template>
  <div id="app">

    <div v-for="(value, key, index) in userProfile" :key="key">
      {{ index }}. {{ key }}: {{ value }}
    </div>

    <div v-for="(courseDetails, courseName) in courses" :key="courseName">
      <div v-for="(value, key) in courseDetails" :key="key">
        {{ courseName }} {{ key }}: {{ value }}
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  data() {
    return {
      userProfile: {
        name: 'John Doe',
        age: 30,
        email: 'john.doe@example.com'
      },
      courses: {
        vue: {
          title: 'Aprender Vue 3',
          author: 'John Doe'
        },
        react: {
          title: 'Aprender React',
          author: 'Jane Doe'
        }
      }
    };
  }
});
</script>

<style scoped>

#app {
  padding: 20px;
  font-family: Arial, sans-serif;
}
div {
  margin-bottom: 10px;
}
</style>