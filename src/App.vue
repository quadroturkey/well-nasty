<template>
  <Header @changePage="changePage"/>
  <Homepage v-show="page == 'home'"/>
  <Film v-show="page == 'film'"/>
  <Workout v-show="page == 'workout'"/>
</template>

<script>
import Header from './components/Header.vue'
import Homepage from './components/Homepage.vue'
import Film from './components/Film.vue'
import Workout from './components/Workout.vue'

export default {
  name: 'App',
  components: {
    Header,
    Homepage,
    Film,
    Workout
  },
  data() {
    return {
      page: 'home',
    }
  },
  methods: {
    changePage(data) {
      this.page = data.link
    }
  }
}
</script>
