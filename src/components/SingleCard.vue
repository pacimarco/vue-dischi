<template>
  <div class="col">
      <div class="card text-center bg-secondary">
      <div class="img-album">
          <img class="album.poster img-fluid card-img-top" :src="album.poster" alt="">
      </div>
      <div class="card-body">
          <h5 class="text-white">{{album.title}}</h5>
      <h6 class="text-dark">{{album.author}}</h6>
      <h6 class="text-dark">{{album.year}}</h6>
      </div>
  </div>
  </div>
</template>

<script>
export default {
name: 'SingleCard',
props:{
    album: Object  //object dà più errori//
}
}
</script>

<style lang="scss">

</style>