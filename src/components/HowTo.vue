<template>
<div class="how-to-container">
  <div class="how-to">
    <div class="how-to-icon-container">
      <One class="how-to-icon" />
    </div>
    <span>Remove the cloves off the garlic head and separate on a flat surface</span>
    <div>
      <img
        class="demo-img"
        src="https://firebasestorage.googleapis.com/v0/b/garlic-rock.appspot.com/o/Demo1_v2.jpg?alt=media&token=73d28c96-1575-4c2f-ad1f-c5d25ee881f3"
        alt=""
      />
    </div>
  </div>
  <div class="how-to">
    <div class="how-to-icon-container">
      <Two class="how-to-icon" />
    </div>
    <span>Hold your Garlic Rock firmly in your hand and smash down on the cloves</span>
    <div>
      <img
        class="demo-img"
        src="https://firebasestorage.googleapis.com/v0/b/garlic-rock.appspot.com/o/Demo2_v2.jpg?alt=media&token=5e1b5739-e09b-4281-9bd8-f0ec4d6c81ed"
        alt=""
      />
    </div>
  </div>
  <div class="how-to">
    <div class="how-to-icon-container">
      <Three class="how-to-icon" />
    </div>
    <span>Now you can easily pick off the loose papery skin from the garlic</span>
    <div>
      <img
        class="demo-img"
        src="https://firebasestorage.googleapis.com/v0/b/garlic-rock.appspot.com/o/Demo3_v2.jpg?alt=media&token=71bbb5ee-25d4-409a-94bf-2e3ac4dd2756"
        alt=""
      />
    </div>
  </div>
  <div class="how-to">
    <div class="how-to-icon-container">
      <Four class="how-to-icon" />
    </div>
    <span>Clean the rock easily in hot soapy water or put it in the dishwasher</span>
  <div>
    <img
      class="demo-img"
      src="https://firebasestorage.googleapis.com/v0/b/garlic-rock.appspot.com/o/Demo4_v2.jpg?alt=media&token=93eb315e-17b3-4e84-aa94-5975b9ff5748"
      alt=""
    />
  </div>
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

.demo-img {
  width: 87%;
  padding-top: 1em;
  padding-bottom: 1em;
  border-radius: 10px;
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
