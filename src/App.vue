<template>
  <div>
    <my-counter v-model="outerCounter"></my-counter>
    <h1> {{ outerCounter }} </h1>
  </div>
</template>

<script>
import MyCounter from './components/MyCounter.vue';

export default {
  name: 'app',
  components: {
    MyCounter,
  },
  data() {
    return {
      outerCounter: 10,
    };
  },
};
</script>

<style>
</style>
