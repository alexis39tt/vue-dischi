<template>
  <main>
    <RecordComp v-for="(elm, i) in records"
        :key="i"
        :image="elm.poster"
        :title="elm.title"
        :author="elm.author"
        :year="elm.year"/>
  </main>
</template>

<script>
import axios from "axios";
import RecordComp from "./RecordComp.vue";

export default {
name: 'MainContainer',
  components: {
    RecordComp
  },
  data(){
      return{
          records: []
      }
  },
  created(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((res) => {
        this.records = res.data.response
        console.log(res.data.response)
      })
      .catch((err) => {
        console.log(err)
      })
  }
};
</script>

<style scoped lang="scss">
$lb: #2e3a46;
main{
    padding: 80px 360px 0;
    display: flex;
    flex-wrap: wrap;
    font-family: Arial, Helvetica, sans-serif;
    justify-content: center;
}
</style>
