<template>
  <div id="app">
    <UserInterface />
  </div>
</template>

<script>
import UserInterface from './components/UserInterface.vue';

export default {
  name: 'App',
  components: {
    UserInterface,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
