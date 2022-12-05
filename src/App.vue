<template>
  <div class="container">

   

    <!-- Step 3 you must use the imported component-->
    <HeaderTop siteTitle= "Top 5 Most Streamed Songs"/>
  <TrackBox :tracks="tracks"/>

  </div>
</template>

<script>
// Step 1: import HeaderTop.vue
import HeaderTop from './components/HeaderTop.vue'
import TrackBox from './components/TrackBox.vue';

export default{

  name: 'App',
    // Step 2: Register the imported component 
    components: {
    HeaderTop,
    TrackBox
  },
  data(){
    return {
      tracks: []
    }
  },
  methods: {
    async fetchTracks(){
      const res = await fetch("https://watery-assorted-brass.glitch.me/api")
      const data = await res.json()
      // console.log(data["songs"])
      return data["songs"]
    }
  },
  async created(){
      this.tracks = await this.fetchTracks()
    }

}
  
</script>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
  *{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body{
    font-family: 'Ivar Text', 'Georgia', serif;
    color: #323954;
  }

  .container{
    max-width: 400px;
    margin:  30px auto;
    overflow: auto;
    min-height: 300px;
    border: 0.3em solid black;
    padding: 30px;
    border-radius: 5px;
  }

</style>