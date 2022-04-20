<template>
    <div class="record">
        <img :src="image" :alt="title">
        <h2>{{ title }}</h2>
        <p>{{ author }}</p>
        <span>{{ year }}</span>
    </div>
</template>

<script>
export default {
  name: 'RecordComp',
  props: {
      image: String,
      title: String,
      author: String,
      year: String
  }
}
</script>

<style scoped lang="scss">
$lb: #2e3a46;
.record{
    background: $lb;
    width: 200px;
    min-width: 200px;
    height: 360px;
    padding: 20px;
    margin: 0 20px 20px;
    text-align: center;
    transition: 0.2s;
    cursor: pointer;
    &:hover{
        transform: translateY(-10px);
        box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.3);
    }
    img{
        max-width: 100%;
    }
    h2{
        color: white;
        margin-top: 18px;
        text-transform: uppercase;
        font-size: 1.3rem;
    }
    p, span{
        color: gray;
        margin-top: 20px;
        font-size: 1.1rem;
    }
}
</style>
