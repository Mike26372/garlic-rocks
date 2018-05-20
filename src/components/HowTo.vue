<template>
<div class="how-to-container">
  <div class="how-to">
    <div class="how-to-icon-container">
      <One class="how-to-icon" />
    </div>
    <span>Remove the cloves off the garlic head and separate on a flat surface</span>
  </div>
  <div class="how-to">
    <div class="how-to-icon-container">
      <Two class="how-to-icon" />
    </div>
    <span>Hold your Garlic Rock firmly in your hand and smash down on the cloves</span>
  </div>
  <div class="how-to">
    <div class="how-to-icon-container">
      <Three class="how-to-icon" />
    </div>
    <span>Now you can easily pick off the loose papery skin from the garlic</span>
  </div>
  <div class="how-to">
    <div class="how-to-icon-container">
      <Four class="how-to-icon" />
    </div>
    <span>Clean the rock easily in hot soapy water or put it in the dishwasher</span>
  </div>
</div>
</template>

<script>
import One from '@/assets/one.svg';
import Two from '@/assets/two.svg';
import Three from '@/assets/three.svg';
import Four from '@/assets/four.svg';
export default {
  name: 'howto',
  components: { One, Two, Three, Four },
};
</script>

<style lang="scss" scoped>
@import '../../static/_main';

div, p {
  font-family: $family-secondary !important;
  font-size: 1.8rem;
  font-weight: 300;
  padding: 1.5rem 0;
  text-align: center;
}

.how-to-container {
  display: flex;
  flex-wrap: wrap;
}

.how-to {
  width: 50%;
  padding: 0 1em;
}

.how-to-icon-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.how-to-icon {
  width: 150px;
  padding-bottom: .5em;
}

@media (max-width: $tablet) {
  .how-to {
    width: 100%;
  }

  .how-to-icon {
    width: 100px;
  }
}
</style>
