<template>
  <div>
    <span class="up-arrow"></span>
  </div>
</template>

<script>
export default {
  name: 'UpArrow',
};
</script>

<style lang="scss" scoped>
  @import '../../static/_main';

  .up-arrow {
    display: block;
    position: absolute;
    content: '';
    width: 100px;
    height: 100px;
    left: 50%;
    margin-left: -50px;
    background-color: $grey-lighter;
    -ms-transform: rotate(45deg);
    -webkit-transform: rotate(45deg);
    transform: rotate(45deg) translate(-35px, -35px);
  }
</style>
