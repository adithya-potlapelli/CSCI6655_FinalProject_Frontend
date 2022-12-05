<template>
<div>
 <h1> {{track.rank}}</h1>
 <h2> {{track.title}}</h2>
 <h2> {{track.streams}} Billion Streams</h2>
 <h2> {{track.year}}</h2>
 <a :href="track.url"><button>Click to Play on YouTube</button></a>
</div>
</template>

<script>
  export default{
    name: 'TrackItem',
    props:{
        track:Array
    }
  }
</script>

<style scoped>
 h4{
    margin:2px;
 }
 div{
    background-color: #f8f1e3;
    color: black;
    padding: 1em;
    margin: 5px;
 }

 button {
  background-color: #ff6c72;
  border: none;
  border-radius: 8px;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
 
}
</style>