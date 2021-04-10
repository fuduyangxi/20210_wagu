<template>
  <div id="app">
    <router-view :yingchang="yingchang" :xianshies="xianshies"/>
    <FooterGuide v-show="xianshi"/>
  </div>
</template>

<script>
import FooterGuide from './components/FooterGuide/FooterGuide'
export default {
  name: 'App',
  data(){
    return{
      xianshi:'true'
    }
  },
  components: {
    FooterGuide
  },
  methods:{
    yingchang(){
      this.xianshi=false;
    },
    xianshies(){
      this.xianshi=true;
    },

  }
}
</script>

<style style lang="stylus" rel="stylesheet/stylus">
  #app
   width 100%
   height 100%
   background #f5f5f5
</style>
