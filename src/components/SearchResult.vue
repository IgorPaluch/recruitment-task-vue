<template>
  <div>
    <h2>Wynik wyszukiwania:</h2>
    <p v-if="result.length === 0">Brak wyników</p>
    <ul v-else>
      <li v-for="number in result" :key="number">{{ number }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    result: Array,
  },
};
</script>
