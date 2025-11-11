 <template>
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
</script> 


