<script>
import TopNavigationBar from './components/TopNavigationBar.vue';
import AppFooter from './components/AppFooter.vue';
import ComicsUtilitiesSection from './components/ComicsUtilitiesSection.vue';
import AppJumbo from './components/AppJumbo.vue';

export default {
  name: 'App',

  components: {
    TopNavigationBar,
    AppFooter,
    ComicsUtilitiesSection,
    AppJumbo,
  }
}
</script>

<template>
  <header>
    <TopNavigationBar />

    <AppJumbo />
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