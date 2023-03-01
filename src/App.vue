<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import AppServices from './components/AppServices.vue'

export default {
  components: {
    AppHeader,
    AppMain,
    AppServices,
    AppFooter,
  }
}


</script>

<template>

  <div>

    <AppHeader />

    <AppMain />

    <AppServices />

    <AppFooter />

  </div>

</template>

<style lang="scss">
@use './style/general.scss' as *;
@use './style/partials/variables' as *;


</style>
