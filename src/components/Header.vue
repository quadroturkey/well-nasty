<template>

  <div class="container">
    <img class="logo" @click="changePage('home')" src="/logo.png">
    <div class="links">
      <a class="link" v-for="link in links" :key="link" @click="changePage(link)">{{ link }}</a>
    </div>
  </div>

</template>

<script>

  export default {
    name: 'Header',
    data() {
      return {
        links: ["home", "film", "workout"]
      }
    },
    methods: {
      changePage(link) {
        this.$emit('changePage', { link })
      }
    }
  }

</script>

<style scoped>

  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 25px 5px;
  }

  .logo {
    width: 75px;
  }

  .links {
    display: flex;
    width: 100%;
    justify-content: space-evenly;
  }

  .link {
    color: #000;
    font-size: 1.5rem;
    text-decoration: none;
    text-transform: capitalize;
    cursor: pointer;
  }

  .link:hover {
    border-bottom: 2px solid var(--dub-red);
  }

</style>
