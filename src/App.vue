<template>
  <div>
    <SearchInput @search-result="updateResult" />
    <SearchResult :result="searchResult" />
  </div>
</template>

<script>
import SearchInput from './components/SearchInput.vue';
import SearchResult from './components/SearchResult.vue';

export default {
  components: {
    SearchInput,
    SearchResult,
  },
  data() {
    return {
      searchResult: [],
    };
  },
  methods: {
    updateResult(result) {
      this.searchResult = result;
    },
  },
};
</script>
