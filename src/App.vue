<script>
import TopNavigationBar from './components/TopNavigationBar.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',

  components: {
    TopNavigationBar,
    AppFooter
  }
}
</script>

<template>
  <header>
    <TopNavigationBar />
  </header>

  <main></main>

  <AppFooter />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
header{
  padding-top: $hgt-top-bar;
}
</style>