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
      <a class="navbar-item">How To Use</a>
      <a class="navbar-item">About Us</a>
      <a class="navbar-item">Heading C</a>
      <a class="navbar-item">BUY NOW</a>
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

  .navbar, .navbar-menu {
    background-color: $grey-lighter !important;
  }

  @media (min-width: $tablet) {
    .navbar-end a {
      transition: color .2s ease;
      padding-top: 18px;
      padding-bottom: 0px !important;
      margin-bottom: 10px;

      &:hover {
        background-color: $grey-lighter !important;
        color: #778899 !important;
        &::after,
        &::before {
          width: 100%;
          left: 0;
        }
      }
    }

    .navbar-end a {
      &::after,
      &::before {
        content: '';
        position: absolute;
        top: calc(100% + 5px);
        width: 0;
        right: 0;
        height: 3px;
      }

      &::before {
        transition: width .4s cubic-bezier(0.51, 0.18, 0, 0.88) .1s;
        background: $grey-darker;
      }

      &::after {
        transition: width .2s cubic-bezier(0.29, 0.18, 0.26, 0.83);
        background: $grey-darker;
      }

    }
  }
</style>
