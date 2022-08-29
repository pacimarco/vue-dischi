<template>
  <div class="container">
      <SingleCard v-for="(album,index) in MyAlbums" :key="index" :album="album"/>
  </div>
</template>

<script>
import axios from 'axios';
import SingleCard from './SingleCard.vue';

export default {
name: 'MyAlbums',
components:{
    SingleCard
},

data(){
    return{
        MyAlbums:[] //error//
    }
},
created(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(response => {
        this.MyAlbums = response.data.response;
        console.log(response.data.response)
    })
}
}
</script>

<style>

</style>