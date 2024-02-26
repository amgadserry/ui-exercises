<template>
  <div class="c-grid">
    <template v-for="row in rows" :key="row">
      <Square v-for="col in cols" :key="col" :active="(col + row) % 2 === 1" :is-main-land="(col + row) % 2 === 1 && (col + row) % 5 === 4" />
    </template>
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
  .c-grid {
    display: grid;
    grid-template-rows: repeat(v-bind(rows), minmax(50px, 1fr));
    grid-template-columns: repeat(v-bind(cols), minmax(50px, 1fr));
    grid-gap: 10px 12px;
  }

</style>
