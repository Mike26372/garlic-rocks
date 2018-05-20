<template>
  <div>
    <span
      class="arrows-down"
      :style="{
        backgroundColor: color,
        boxShadow: `-50px 50px 0 ${color}, 50px -50px 0 ${color}`
      }">
    </span>
  </div>
</template>

<script>
export default {
  name: 'ArrowsDown',
  props: ['color'],
};
</script>

<style lang="scss" scoped>
  @import '../../static/_main';

  .arrows-down {
    display:block;
    position:absolute;
    content:'';
    left: 50%;
    width: 50px;
    height: 50px;
    -webkit-transform: translateX(-50%) rotate(45deg);
    transform: translateX(-50%) translateY(-25px) rotate(45deg);
    z-index: 10;
    background-color: $white;
  }
</style>
