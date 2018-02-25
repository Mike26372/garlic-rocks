<template>
  <nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item link" href="/">
      <LogoSmall class="garlic-logo-small" />
    </a>
    <span class="navbar-item">
      garlicrocks.com
    </span>
    <span class="navbar-item is-hidden-desktop link">
      <span class="button is-white">BUY NOW</span>
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
      <a class="navbar-item link underline" href="#how-to">
        <span>How To Use</span>
      </a>
      <a class="navbar-item link underline" href="#why">
        <span>Why A Rock?</span>
      </a>
      <a class="navbar-item link underline" href="#about">
        <span>About Us</span>
      </a>
      <a class="navbar-item link is-hidden-touch">
        <span class="button is-white">BUY NOW</span>
      </a>
    </div>
  </div>
</nav>
</template>

<script>
import LogoSmall from '@/assets/garlic_rock_logo_small.svg';

export default {
  name: 'NavBar',
  template: '<NavBar />',
  components: {
    LogoSmall,
  },
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

  .navbar, .navbar-menu, .navbar-item {
    // background-color: $grey-darker !important;
    background-color: $black !important;
    color: $grey-lighter !important;
  }

  .link {
    color: $grey-lighter !important;
    &:hover {
      background-color: $grey-darker !important;
      color: #778899 !important;
    }
  }

  .garlic-logo-small {
    fill: white;
    width: 20px;
  }

  span.button {
    &:hover,
    &:focus {
      color: $white !important;
      background-color: $grey-darker !important;
      border: 1px solid white !important;
      font-weight: 600;
    }
  }

  @media (min-width: $tablet) {
    .underline {
      transition: color .2s ease;

      &:hover {
        background-color: $grey-darker !important;
        color: #778899 !important;
        &::after,
        &::before {
          width: 100%;
          left: 0;
        }
      }
    }

    .underline {
      &::after,
      &::before {
        content: '';
        position: absolute;
        top: calc(100% - 2px);
        width: 0;
        right: 0;
        height: 3px;
      }

      &::before {
        transition: width .4s cubic-bezier(0.51, 0.18, 0, 0.88) .1s;
        background: $grey-lighter;
      }

      &::after {
        transition: width .2s cubic-bezier(0.29, 0.18, 0.26, 0.83);
        background: $grey-lighter;
      }

    }
  }
</style>
