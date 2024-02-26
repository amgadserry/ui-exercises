<template>
  <div :class="['c-square', { 'c-square--active': active, 'c-square--inactive': !active, 'c-square--main-land': isMainLand }]">
    <div v-if="isMainLand" class="c-squar__text">M</div>
  </div>
</template>

<script>
export default {
  name: "CSquare",
  props: {
    active: {
      type: Boolean,
      default: false
    },
    isMainLand: {
      type: Boolean,
      default: false
    }
  },
};
</script>

<style scoped>
.c-square {
  aspect-ratio: 1;
  background-color: #D9D9D9;
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  border: 5px solid transparent;
  transition: all 250ms ease-in-out;
  opacity: 1;
  z-index: 1;
}
.c-square--active {
  background-color: #FF7171;
}
.c-squar__text {
  font-weight: bold;
  font-size: 32px;
  color: white;
}

.c-square:hover {
  transform: scale(1.5);
  z-index: 5;
  border-radius: 20px;
}
.c-square--active:hover {
  border-radius: 15px;
  border: 5px solid #A0A0A0;
  background-color: #FF7171;
  opacity: 1;
  box-shadow: none;
}
.c-square--inactive:hover {
  opacity: 0.6;
  background-color: black;
  box-shadow: 0px 4px 10px 5px rgba(0, 0, 0, 0.47);
}
</style>
