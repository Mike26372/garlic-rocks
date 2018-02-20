<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="/">
      <img src="@/assets/garlic_download.png" />
    </a>
    <span class="navbar-item">
      GarlicRocks.com
    </span>
    <div
      class="navbar-burger"
      v-bind:class="{ 'is-active': isActive }"
      v-on:click="toggleActive()"
    >
      <span></span>
      <span></span>
      <span></span>
    </div>
  </div>
  <div class="navbar-menu" v-bind:class="{ 'is-active': isActive }">
    <div class="navbar-start">

    </div>
    <div class="navbar-end">
      <span class="navbar-item">How To Use</span>
      <span class="navbar-item">About Us</span>
      <span class="navbar-item">Heading C</span>
      <span class="navbar-item">BUY NOW</span>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  name: 'NavBar',
  template: '<NavBar />',
  data() {
    return { isActive: false };
  },
  methods: {
    toggleActive: function toggleActive() {
      // eslint-disable-next-line
      console.log('TOGGLED');
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style lang="scss">
  @import '../../static/_main';

  .navbar {
    background-color: $grey-lighter !important;
  }
</style>
