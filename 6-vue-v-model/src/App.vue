<template>
  <div>
    <input v-model.trim="username" />

    <input type="checkbox" v-model="isChecked" />

    <input v-model.lazy="email" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "john_doe",
      isChecked: false,
      email: "john.doe@example.com",
    };
  },
};
</script>
