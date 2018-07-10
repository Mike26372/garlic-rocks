<template>
<div>
  <div>
    We are a family from the Central Valley of Northern California
    that loves cooking with fresh, wholesome ingredients
  </div>
  <div>
    Garlic is one of our favorite ingredients
    and for over 15 years we have been using a rock to
    crush garlic and easily remove the papery skin
  </div>
  <div class="secondary-font">
    So we decided to share our favorite kitchen tool with you!
  </div>

  <!-- <p>
    Terri: Our business coordinator
    Kim: Our rock engraver
    Natalie: Garlic Rock’s spokesperson in demonstration video
    Kevin: Our finance guy
    Michael: Website designer
  </p> -->
</div>
</template>

<script>
export default {
  name: 'about',
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

.secondary-font {
  font-family: $family-primary !important;
  font-style: italic;
}
</style>
