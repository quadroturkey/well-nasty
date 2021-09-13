<template>
  <Header/>
  <Homepage v-show="page == 'homepage'"/>
</template>

<script>
import Header from './components/Header.vue'
import Homepage from './components/Homepage.vue'

export default {
  name: 'App',
  components: {
    Header,
    Homepage
  },
  data() {
    return {
      page: 'homepage',
    }
  }
}
</script>
