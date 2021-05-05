<template>
  <Profile />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Profile from "./components/Profile.vue";

export default defineComponent({
  name: 'App',
  components: {
    Profile,
  }
});
</script>

<style>
#app {
  box-sizing: border-box;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 60px 40px;
  max-width: 800px;
}
</style>
