<template>
  <div class="card">
      <div class="img-album">
          <img :src="album.poster" alt="">
      </div>
      <h4>{{album.title}}</h4>
      <h6>{{album.author}}</h6>
      <h6>{{album.year}}</h6>
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

<style>

</style>