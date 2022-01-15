<template>
  <div>
    <Header/>
    <SnackView/>
    <Snack-data/>
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
    SnackData,
  },
  name: 'IndexPage'
}
</script>
