<template>
  <div id="app">
   <MyHeader :message="'prova'"/>
   <MyAlbums/>
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
    
}
}
</script>

<style lang="scss">
@import '@/styles/general.scss';
</style>
