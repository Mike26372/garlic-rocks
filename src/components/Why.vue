<template>
<div>
  <div>
    If a rock is sized and perfectly weighted,
    it is absolutely the best way to safely crush and peel garlic cloves
  </div>
  <div class="secondary-font">
    No sharp edges to cut yourself on | No nooks and crannies
    that are difficult to clean
  </div>
  <div class="video">
    <iframe
      src="https://www.youtube.com/embed/TpdlJVNZRxI"
      frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    >
    </iframe>
  </div>
</div>
</template>

<script>
export default {
  name: 'why',
};
</script>

<style lang="scss" scoped>
@import "../../static/_main";

div,
p {
  font-family: $family-secondary !important;
  font-size: 1.8rem;
  font-weight: 300;
  padding: 1.5rem 0;
  text-align: center;
}

.secondary-font {
  font-family: $family-primary !important;
  font-style: italic;
}

.video {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 */
  width: 100%;
  height: 0;

  iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
}
</style>
