<template>
  <div class="two-lines"></div>
</template>

<script>
export default {
  name: 'TwoLines',
};
</script>

<style lang="scss" scoped>
  @import '../../static/_main';

  .two-lines {
    display: block;
    position: absolute;
    content: '';
    width: 100px;
    height: 1px;
    left: 50%;
    -webkit-transform: translateX(-50%);
    transform: translateX(-50%);
    background: $grey-darker;
    box-shadow: 0 8px 0 $grey-darker;
  }
</style>
