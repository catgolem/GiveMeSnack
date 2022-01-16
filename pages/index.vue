<template>
  <div class="home-background pb-12">
    <Header/>
    <SnackView/>
    <Snack-data class="text-shadow-sm"/>
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import SnackView from '../components/SnackView.vue'
import SnackData from '../components/SnackData.vue'

export default {
  components: { 
    Header,
    SnackView ,
    SnackData
  },
  name: 'IndexPage'
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Hachi+Maru+Pop&family=Zen+Maru+Gothic:wght@500&display=swap');
* {
  font-family: 'Hachi Maru Pop', cursive;
}
.home-background{
  background: repeating-linear-gradient(-45deg, #d0546a22, #d0546a22 40px, #d0546a 40px, #d0546a 80px);
}
</style>