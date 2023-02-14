<template>
  <div id="app">
    <HeaderPart />
    <BodyPart />
    <FooterTB />
  </div>
</template>

<script>
import HeaderPart from './components/Head.vue'
import BodyPart from '../src/components/Body/Body.vue'
import FooterTB from './components/FooterTB.vue'

export default {
  name: 'App',
  components: {
    HeaderPart,
    BodyPart,
    FooterTB
  }
}
</script>

<style scoped>
#app {
  padding: -10;
  margin: -10;
}
</style>
