<template>
  <header>
    <img src="../assets/spotify.png" alt="logo">
    <select>
      <option v-for="(elm, i) in array" value="elm" :key="i">{{ elm }}</option>
    </select>
  </header>
</template>

<script>
export default {
  name: 'HeadBar',
  data(){
    return{
      array: ['1', 'dieci']
    }
  }
}
</script>

<style scoped lang="scss">
$lb: #2e3a46;
header{
  height: 70px;
  padding: 12px 22px;
  background: $lb;
  img{
    max-height: 100%;
  }
  select{
    height: 30px;
    margin: 8px 0;
    padding: 0 3px;
    float: right;
    font-size: 1.2rem;
    outline: none;
  }
}
</style>
