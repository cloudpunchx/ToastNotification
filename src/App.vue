<template>
  <div id="app">
    <ToastNotification/>
    <PostButton/>
    <DeleteButton/>
  </div>
</template>

<script>
import ToastNotification from '@/components/ToastNotification.vue';
import PostButton from '@/components/PostButton.vue';
import DeleteButton from '@/components/DeleteButton.vue';
export default {
      name: 'App',
      components: {
        ToastNotification,
        PostButton,
        DeleteButton,
      }
  }
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
