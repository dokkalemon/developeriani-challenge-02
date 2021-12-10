<template>
  <div id="app">
    <Card v-for="(item, index) in infoCard" :key="`card${index}`"
    :thumb="item.thumb"
    :title="item.title"
    :text="item.text"
    :logoValue="item.logoValue"
    :value="item.value"
    :typeValue="item.typeValue"
    :time="item.time"
    :avatar="item.avatar"
    :name="item.name"
    :url="item.url"
    />
    


    

  </div>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  },

  data() {
    return {
      infoCard: [
        {
          thumb: 'image-equilibrium.jpg',
          title: 'Equilibrium #3429',
          text: 'Our Equilibrium collection promotes balance and calm.',
          logoValue: 'icon-ethereum.svg',
          value: '0.041',
          typeValue: 'ETH',
          time: '3 days left',
          avatar: 'image-avatar.png',
          name: 'Jules Wyvern',
          url: 'https://github.com/dokkalemon'
        },
        
        ]
    }
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
