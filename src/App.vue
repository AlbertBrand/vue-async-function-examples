<template>
  <div id="app">
    <button @click="show = !show">Show / hide components</button>
    <SimpleUseAsyncComponent v-if="show" />
    <UseAsyncComponent v-if="show" />
    <UseFetchComponent v-if="show" />
  </div>
</template>

<script>
import SimpleUseAsyncComponent from "./components/SimpleUseAsyncComponent.vue";
import UseAsyncComponent from "./components/UseAsyncComponent.vue";
import UseFetchComponent from "./components/UseFetchComponent.vue";

export default {
  name: "app",
  data() {
    return {
      show: true
    };
  },
  components: {
    SimpleUseAsyncComponent,
    UseAsyncComponent,
    UseFetchComponent
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: #2c3e50;
}
</style>
