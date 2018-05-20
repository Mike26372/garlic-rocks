<template>
  <div>
    <TopCurveSVG />
  </div>
</template>

<script>
import TopCurveSVG from '@/assets/top_curve.svg';

export default {
  name: 'TopCurve',
  components: { TopCurveSVG },
};
</script>

<style lang="scss" scoped>
  @import '../../static/_main';

  #top-curve {
    position: absolute;
    padding-top:0;
    margin-top:0;
    fill: $black;
    stroke: $black;
    width: 100%;
    transform: translateY(-100px) rotate(180deg);
  }
</style>
