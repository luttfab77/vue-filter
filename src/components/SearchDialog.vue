<template>
  <div>
    <ul>
      <li v-for="item in filteredItems">
        <a :href="item.Page" target="_blank"> {{ item.Name }} </a>
      </li>
    </ul>
  </div>
</template>

<script>
import titles from '../post-data.json';
import { computed } from 'vue';
export default {
  props: {
    query: String,
  },
  setup(props, context) {
    const filteredItems = computed(() => {
      return titles.filter((s) =>
        s.Name.toLowerCase().includes(props.query.toLowerCase())
      );
    });
    return {
      titles,
      filteredItems,
    };
  },
};
</script>

<style scoped></style>
