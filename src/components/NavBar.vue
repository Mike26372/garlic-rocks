<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="/">
      <img src="@/assets/garlic_download.png" />
    </a>
    <span class="navbar-item">
      GarlicRocks.com
    </span>
    <div class="navbar-burger">
      <span class="navbar-item">How To Use</span>
      <span class="navbar-item">About Us</span>
      <span class="navbar-item">Heading C</span>
      <span class="navbar-item">BUY NOW</span>
    </div>
  </div>
  <div class="navbar-menu">
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
};
</script>

<style lang="postcss">

</style>
