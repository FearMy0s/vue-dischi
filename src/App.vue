<template>
  <div id="app">
    <diskHeader/>
    <diskMain/>

  </div>
</template>

<script>
import diskHeader from './components/blocks/diskHeader.vue';
import diskMain from './components/blocks/diskMain.vue';
export default {
  name: 'App',
  components: {
    diskHeader,
    diskMain,
  }
}
</script>

<style lang="scss">
@import './assets/style/global.scss';
</style>
