<template>

  <div class="container">
    <img class="logo" src="/logo.png">
    <div class="links">
      <a class="link" v-for="link in links" :key="link" :href="'/' + link" @click="navigate(link)">{{ link }}</a>
    </div>
  </div>

</template>

<script>

import '../styles/header.css'

export default {
  name: 'Header',
  data() {
    return {
      links: ["home", "film", "workout"]
    }
  }
}

</script>
