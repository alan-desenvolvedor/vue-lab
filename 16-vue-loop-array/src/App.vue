<!-- <template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="item.id">
        {{ index }}: {{ item.name }} costs ${{ item.price }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { id: 1, name: 'Maça', price: 1.2 },
        { id: 2, name: 'Banana', price: 0.8 },
        { id: 3, name: 'Pera', price: 2.0 },
      ],
    };
  },
};
</script> -->

<!-- ACESSANDO O LOOP INDEX -->

<!-- <template>
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
</style> -->

<!-- ACESSANDO OBJETO -->
<!-- <template>
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
</style> -->

<!-- LOOP NUMERAÇÃO -->
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
