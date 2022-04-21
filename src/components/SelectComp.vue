<template>
  <select v-model="selected">
    <option v-for="(elm, i) in filter()" value="elm" :key="i">{{ elm }}</option>
  </select>
</template>
<script>
export default {
  name: "SelectComp",
  props: {
    records: Array,
  },
  data() {
    return {
      filtered: [],
      selected: "",
    };
  },
  methods: {
    filter() {
      this.records.forEach((elm) => {
        if (!this.filtered.includes(elm.genre)) {
          this.filtered.push(elm.genre);
        }
      });
      return this.filtered;
    },
  }
};
</script>
<style lang="scss" scoped>
select {
  position: absolute;
  top: 20px;
  height: 30px;
  right: 22px;
  padding: 0 5px;
  font-size: 1.2rem;
  outline: none;
}
</style>