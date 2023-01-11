<script>
import AppMain from './components/AppMain.vue'

export default {
  components: {
    AppMain
  },
}
</script>

<template>
  <main>
    <AppMain />
  </main>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;

main {
  max-width: 1700px;
  margin: 0 auto;
  text-align: center;
}
</style>
