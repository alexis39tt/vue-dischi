<template>
  <header>
    <img src="../assets/spotify.png" alt="logo">
  </header>
</template>

<script>
export default {
  name: 'HeadBar'
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
}
</style>
