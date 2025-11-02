<template>
  <div>
    <form @submit.prevent="updateComment">
      <textarea v-model="userInput"></textarea>
      <button type="submit">Submit</button>
    </form>
    <p v-html="sanitizedComment"></p>
  </div>
</template>

<script>
import DOMPurify from 'dompurify';

export default {
  data() {
    return {
      userInput: '',
      userComment: ''
    };
  },
  computed: {
    sanitizedComment() {
      return DOMPurify.sanitize(this.userComment);
    }
  },
  methods: {
    updateComment() {
      this.userComment = this.userInput;
    }
  }
};
</script>