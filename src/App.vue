<template>
  <div id="app">
    <HeadBar />
    <MainContainer />
  </div>
</template>

<script>
import HeadBar from "./components/HeadBar.vue";
import MainContainer from "./components/MainContainer.vue";

export default {
  name: 'App',
  components: {
    HeadBar,
    MainContainer
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  background: #1e2d3b;
}
</style>
