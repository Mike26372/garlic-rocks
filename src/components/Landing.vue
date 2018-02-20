<template>
  <div class="hero is-dark is-large">
    <div class="hero-body">
      <div class="container">
        <h1 class="title">
          {{ header }}
        </h1>
        <h2 class="subtitle">
          {{ subheader }}
        </h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Landing',
  data() {
    return {
      header: 'GarlicRocks.com',
      subheader: 'The natural kitchen essential for garlic lovers',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  @import '../../static/_main';
  .subtitle {
    font-family: $family-secondary !important;
  }

  @media (max-width: $tablet) {
    .hero {
      height: 100vh;
      max-height: 800px;
    }

    .hero-body {
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
  }
</style>
