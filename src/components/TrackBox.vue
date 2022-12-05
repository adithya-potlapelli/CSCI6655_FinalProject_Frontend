<template>
    <div v-for="track in tracks" :key="track.rank" >
        <TrackItem :track="track"/>
    </div>

</template>

<script>
import TrackItem from './TrackItem.vue';
 export default{
    name: 'TrackBox',
    components: {
        TrackItem
    },
    props:{
        tracks:Array
    }
 }
</script>

<style scoped>

.bookbox{
    background-color: bisque;
    padding: 1em;
    color: gray;
}
</style>