<template>
  <custom-button>click me</custom-button>
  <!-- <starwars-header>스타워즈</starwars-header> -->
  <starwars-header>
    <template v-slot:title>
      슬롯 타이틀
    </template>
    <template v-slot:subject>
      슬롯 서브젝트
    </template>
  </starwars-header>
  <starwars-main></starwars-main>
  <starwars-footer></starwars-footer>
  {{rarara}}
</template>

<script>
import StarwarsFooter from './components/StarwarsFooter.vue'
import StarwarsHeader from './components/StarwarsHeader.vue'
import StarwarsMain from './components/StarwarsMain.vue'

import debug from './mixins/debug.js'

export default {
  name: 'App',
  components: {
    StarwarsFooter,
    StarwarsMain,
    StarwarsHeader,
  },
  mixins: [debug],
  data(){
    return{
      myObj:{
        some: 'data',
        other: 'values'
      }
    }
  },
  created(){
    console.log(this.debug(this.myObj))
  }
}
</script>

<style>
</style>
