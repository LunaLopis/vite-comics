
<script>
import AppSeries from './components/AppSeries.vue';
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    AppSeries,
    AppMain,
    AppFooter,

  }
}
</script>

<template lang="">
  <div>
    <AppHeader />
    <AppSeries />
    <AppMain />
    <AppFooter />
  </div>
</template>

<style lang="scss">
@use './styles/generals.scss' as *;
</style>