<template>
    <div class="col">
        <div class="card text-center bg-secondary">
        <div class="img-album img-fluid">
            <img class="album-poster img-fluid img-thumbnail card-img-top" :src="album.poster" alt="">
        </div>
        <div class="card-body">
            <h5 class="text-white card-title">{{album.title}}</h5>
        <h6 class="text-dark card-text">{{album.author}}</h6>
        <h6 class="text-dark card-text">{{album.year}}</h6>
        </div>
    </div>
    </div>
  </template>
  
  <script>
  export default {
  name: 'SingleCard',
  props:{
      album: Object  
  }
  }
  </script>
  
  <style lang="scss">
  </style>