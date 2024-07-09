<script>
import TopNavigationBar from './components/TopNavigationBar.vue';

export default {
  name: 'App',

  components: {
    TopNavigationBar,
  }
}
</script>

<template>
  <header>
    <TopNavigationBar />
  </header>
  <main></main>
  <footer></footer>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
header{
  padding-top: $hgt-top-bar;
}
</style>