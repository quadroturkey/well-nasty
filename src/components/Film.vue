<template>

  <div class="video-grid">
    <div class="video-wrap" v-for="(video, index) in videos" :key="index">
      <iframe class="video" width="320" height="240" :src="'https://www.youtube.com/embed/' + video.id + '?start=0'" title="video.title" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      <h6 class="video-title">{{ video.title }}</h6>
    </div>
  </div>

</template>

<style scoped>

  .video-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    margin: 10px 25px;
  }

  .video-title {
    margin: 5px 0 20px;
    text-align: start;
    font-family: "Montserrat", sans-serif;
    font-weight: 300;
    letter-spacing: .5px;
    max-width: 320px;
  }

</style>

<script>

  export default {
    name: 'Film',
    data() {
      return {
        videos: [
          {
            title: "Austin Doublewide vs Raleigh Ring of Fire--2019 National Championships",
            id: "gBZfep7aSMk",
          },
          {
            title: "Toronto GOAT vs Austin Doublewide - 2014 Chesapeake Invite - Pool Play (M)",
            id: "Fq-uLo0s4QY"
          },
          {
            title: "San Francisco Revolver vs Austin Doublewide - 2012 USAU Club Nationals - Final (M)",
            id: "v_Eg_wducP0"
          },
          {
            title: "Boston Ironside vs Austin Doublewide - 2012 USAU Club Nationals - Semifinal (M)",
            id: "M4RdZjqF_HE"
          },
          {
            title: "Rhino vs Doublewide - 2012 Labor Day Championships",
            id: "TgKfwRnYf4Y"
          },
          {
            title: "Doublewide vs Johnny Bravo - 2012 Labor Day Ultimate Championships - Semifinal (M)",
            id: "5EBa-E57ZC0"
          },
          {
            title: "H.I.P. vs Doublewide - 2019 South Central Club Regionals - 1st Place Semis",
            id: "XB1YqFX4RYI"
          },
          {
            title: "San Francisco Revolver vs Austin Doublewide | 2017 Club National Championships",
            id: "RirpYssVAw8"
          },
          {
            title: "San Francisco Revolver vs Austin Doublewide - 2012 USAU Club Nationals - Final (M)",
            id: "RirpYssVAw8"
          },
          {
            title: "NexGen vs Austin Doublewide - 2012 NexGen Ultimate Tour",
            id: "srXrkN5Q12Q"
          },
          {
            title: "2019 USAU Club Nationals - Pool Play - Ring of Fire vs. Doublewide",
            id: "Ad7V483BPgE"
          },
        ]
      }
    },
  }

</script>
