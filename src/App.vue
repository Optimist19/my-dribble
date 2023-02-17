<template>
  <div id="app">
    <HeaderPart />
    <BodyPart />
    <FooterTB />
    <FooterFB />
  </div>
</template>

<script>
import HeaderPart from './components/Head.vue'
import BodyPart from '../src/components/Body/Body.vue'
import FooterTB from './components/Footer/FooterTB.vue'
import FooterFB from './components/Footer/FooterFB.vue'

export default {
  name: 'App',
  components: {
    HeaderPart,
    BodyPart,
    FooterTB,
    FooterFB
  }
}
</script>

<style scoped>
#app {
  padding: -10;
  margin: -10;
}
</style>
