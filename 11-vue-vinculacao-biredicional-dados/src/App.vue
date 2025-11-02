<template>
  <div>
    <input v-model="message1">
    <p>Message1: {{ message1 }}</p>
    
    <textarea v-model="message2"></textarea>
    <p>Character Count: {{ message2.length }}</p>
    
    <select v-model="selectedOption">
      <option disabled value="">Please select one</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
    <p>Selected: {{ selectedOption }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message1: 'Hello!',
      message2: '',
      selectedOption: ''
    };
  }
};
</script>