<template>
  <!--input type="text" v-model="input" placeholder="Search..." / -->
  <img alt="Vue logo" src="https://vuejs.org/images/logo.png" />
  <div>
    <h1>Articles</h1>
    <input type="text" v-model="query" placeholder="Search" />
    <br />
    <button @click="resetInput">Reset</button>
    <SearchDialog :query="query" />
  </div>
</template>

<script>
import { ref } from 'vue';
import SearchDialog from './SearchDialog.vue';

export default {
  components: {
    SearchDialog,
  },

  setup() {
    const query = ref('');

    function resetInput() {
      query.value = '';
    }

    return {
      query,
      resetInput,
    };
  },
};
</script>

<style scoped>
img {
  width: 5em;
}
input[type='text'] {
  margin-bottom: 20px;
  padding: 5px;
}
</style>
