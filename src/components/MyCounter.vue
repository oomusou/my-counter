<template>
  <div>
    <h1>{{ innerCounter }}</h1>
    <button @click="add">+1</button>
    <button @click="emit">Emit Counter</button>
  </div>
</template>

<script>
export default {
  name: 'MyCounter',
  props: [
    'value',
  ],
  data() {
    return {
      innerCounter: this.value,
    };
  },
  methods: {
    add() {
      this.innerCounter += 1;
    },
    emit() {
      this.$emit('input', this.innerCounter);
    },
  },
};
</script>

<style scoped>

</style>
