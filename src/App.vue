<script>
import AppMain from './components/AppMain.vue'
import AppHeader from './components/AppHeader.vue'


export default {
  components: {
    AppMain,
    AppHeader,
  },
}
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main>
    <AppMain />
  </main>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;

main {
  background-color: rebeccapurple;
}
</style>
