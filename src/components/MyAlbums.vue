<template>
    <div class="container bg-dark">
        <div class="row row-cols-5 g-3">
            <SingleCard v-for="(album,index) in MyAlbums" :key="index" :album="album"/>
        </div>
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
  props: {
        userGenreSelected: String
    },
  data(){
      return{
          MyAlbums:[] 
      }
  },
  created(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then(response => {
          this.MyAlbums = response.data.response;
          console.log(response.data.response)
      })
  },
  computed: {
        filterGenreSelectedByUser(){
            if (this.userGenreSelected === undefined) {
                return this.musicList;
            }
            return this.musicList.filter((album) => {
                return album.genre.toLowerCase().includes(this.userGenreSelected)
            });
        }
    }
  }
  </script>
  
  <style>