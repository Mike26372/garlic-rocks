<template>
  <div id="app">
    <NavBar />
    <router-view/>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar';

export default {
  name: 'App',
  components: {
    NavBar,
  },
};
</script>

<style lang="scss">
@import '../static/_main';

#app {
  background-color: $grey-lighter;
  // width: 100vw;
}
</style>

