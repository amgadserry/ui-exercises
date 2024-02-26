<template>
  <div class="c-grid">
    <div class="c-row" v-for="row in rows" :key="row">
      <Square v-for="col in cols" :key="col" />
    </div>
  </div>
</template>

<script>
import Square from "./Square";
export default {
  name: "CGrid",
  components: { Square },
  props: {
    rows: {
      type: Number,
      default: 5,
    },
    cols: {
      type: Number,
      default: 5,
    },
  },
};
</script>

<style scoped>
</style>
