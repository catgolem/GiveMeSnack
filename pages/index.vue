<template>
  <div>
    <Header/>
    <SnackView/>
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import SnackView from '../components/SnackView.vue'

export default {
  components: { 
    Header,
    SnackView 
  },
  name: 'IndexPage'
}
</script>
