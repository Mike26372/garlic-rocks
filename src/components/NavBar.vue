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
      <span class="button is-white" v-on:click="toggleModal()">BUY NOW</span>
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
        <span class="button is-white" v-on:click="toggleModal()">BUY NOW</span>
      </a>
    </div>
  </div>
  <div class="modal-container" :style="{display: isModalShown ? 'block' : 'none'}">
    <div class="modal-contents">
      <div class="modal-inner-container">
        <div class="delete-button" v-on:click="toggleModal()">
          <i class="fas fa-times"></i>
        </div>
        <Shopify />
      </div>
    </div>
  </div>
</nav>

</template>

<script>
import LogoSmall from '@/assets/garlic_rock_logo_small.svg';
import Shopify from '@/components/Shopify';

export default {
  name: 'NavBar',
  template: '<NavBar />',
  components: {
    LogoSmall,
    Shopify,
  },
  data() {
    return { isActive: false, isModalShown: false };
  },
  methods: {
    toggleActive: function toggleActive() {
      // eslint-disable-next-line
      this.isActive = !this.isActive;
    },
    toggleModal: function toggleModal() {
      this.isModalShown = !this.isModalShown;
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

  .modal-inner-container {
    position: relative;
    width: 100%;
  }

  .delete-button {
    position: absolute;
    top: 0;
    right: 0;
    transform: translate(12px, -16px);
    color: #363636;
    cursor: pointer;
  }

  .modal-container {
    display: block;
    position: fixed;
    padding: 0 1em;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.4);
  }

  .modal-contents {
    background-color: white;
    border-radius: 3px;
    margin: 20% auto;
    max-width: 600px;
    padding: 1.5em;
    border: 1px solid #363636;
    width: 60%;

    iframe {
      min-height: 350px !important;
    }
  }

  @media (max-width: $tablet) {
    .modal-contents {
      margin: 20% auto;
      width: 100%;

      iframe {
        min-height: 850px !important;
      }
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
