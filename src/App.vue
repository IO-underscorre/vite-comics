<script>
import TopNavigationBar from './components/TopNavigationBar.vue';
import AppFooter from './components/AppFooter.vue';
import ComicsUtilitiesSection from './components/ComicsUtilitiesSection.vue';

export default {
  name: 'App',

  components: {
    TopNavigationBar,
    AppFooter,
    ComicsUtilitiesSection
  }
}
</script>

<template>
  <header>
    <TopNavigationBar />
  </header>

  <main>
    <ComicsUtilitiesSection />
  </main>

  <AppFooter />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
header{
  padding-top: $hgt-top-bar;
}
</style>