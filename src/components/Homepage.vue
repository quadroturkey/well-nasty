<template>
  
  <div class="container">
    <div class="video-wrapper">
      <video width="320" height="240" autoplay loop muted>
        <source src="../assets/home-background.mp4" type="video/mp4">
        Your browser does not support video tag
      </video>
      <button class="film-btn" @click="changePage('film')">film room</button>
    </div>
  </div>

</template>

<script>

  export default {
  name: 'Homepage',
  data() {
    return {
      
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
    height: calc(100vh - 85px);
    background-color: var(--dub-blue);
    display: flex;
    align-items: center;
  }

  .video-wrapper {
    position: relative;
    width: 100vw;
  }

  video {
    min-width: 100%;
    height: auto;
    max-height: 575px;
    object-fit: cover;
  }

  .film-btn {
    position: absolute;
    left: 50%;
    top: 50%;
    background-color: var(--dub-red);
    color: #fff;
    border: none;
    padding: 0.75em;
    font-size: 0.8rem;
    font-weight: 500;
    font-family: "Montserrat", sans-serif;
    text-transform: uppercase;
    transform: translate(-50%, -50%);
  }

</style>