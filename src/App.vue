<template>
  <div id="app">
   <MyHeader @genre="genreSelected"/>
   <MyAlbums :userGenreSelected="genreSelectedByUser"/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyAlbums from './components/MyAlbums.vue';
export default {
  name: 'App',
  components: {
    MyHeader,
    MyAlbums,
    
},
data: function(){
    return{
      genreSelectedByUser: undefined,
    }
  },
  methods: {
    genreSelected(selected){
      this.genreSelectedByUser = selected;
    }
  }
}
</script>

<style lang="scss">
@import '@/styles/general.scss';
</style>