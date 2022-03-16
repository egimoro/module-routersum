<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
    };
  },
  methods: {
    increment() {
      return parseFloat(this.num1) + parseFloat(this.num2);
    },
  },
};
</script>

<template>
  <div>
    <input v-model="num1" placeholder="First number" />
    <p>{{ num1 }}</p>
    <input v-model="num2" placeholder="Second number" />
    <p>{{ num2 }}</p>
    <hr />
    <p>{{ increment() }}</p>
  </div>
</template>
