<template>
  <div id="app">
    <Card />
    

  </div>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  }
}
</script>

<style lang="scss">
@import '@/styles/global.scss';

#app {
  height: 100vh;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;

}



</style>
