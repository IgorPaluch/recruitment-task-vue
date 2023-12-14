<template>
  <div>
    <input v-model="inputText" placeholder="Wprowadź liczby po przecinku" />
    <button @click="search">Wyszukaj</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
    };
  },
  methods: {
    search() {
      const numbers = this.inputText.split(',').map(Number);
      const oddNumbers = numbers.filter(num => num % 2 !== 0);
      this.$emit('search-result', oddNumbers);
    },
  },
};
</script>
