<template>
  <header>
    <div @click="goto('home')">FootCat</div>
    <nav>
      <div @click="goto('restaurant')">restaurant</div>
      <div @click="goto('drinks')">drinks</div>
      <div id="fav">
        favourite
        <div id="item">111</div>
      </div>
    </nav>
    <div>user</div>
  </header>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    goto(where) {
      this.$router.replace(where);
    },
  },
};
</script>

<style lang="css">
header {
  width: 100vw;
  height: 10vh;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: space-around;
  background-color: antiquewhite;
}
nav {
  width: 20vw;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

nav > div {
  width: 200px;
  /* height: 100%; */
  line-height: 100%;
  text-align: center;
}

#fav:hover {
  background-color: rgb(127, 117, 103);
}

#fav > #item {
  position: absolute;
  width: 0px;
  height: 0px;
  overflow: hidden;
}

#fav:hover #item {
  width: 100px;
  height: 100px;
  transition: 0.5s;

  background-color: rgb(127, 117, 103);
}
</style>
