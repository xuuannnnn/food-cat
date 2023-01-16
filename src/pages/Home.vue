<template>
  <div>
    <div>Here is foodcat restaurant review website</div>
    <button @click="goto('login')">login click here!</button>
    <button @click="goto('restaurant')">restaurant review click here!</button>
    <button @click="goto('drinks')">drink review click here!</button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    goto(where) {
      this.$router.push(where);
    },
  },
};
</script>
