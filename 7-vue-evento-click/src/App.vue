<template>
  <div>
    <form @submit.prevent="submitForm">
      <input v-model.trim="username" />
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: ""
    };
  },
  methods: {
    submitForm() {
      alert(`Hello, ${this.username}`);
    }
  }
};
</script>