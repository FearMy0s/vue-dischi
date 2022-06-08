<template>
  <header>
      <div class="container">
          <img src="https://upload.wikimedia.org/wikipedia/commons/8/84/Spotify_icon.svg" alt="">
      <SearchDisk/>
      </div>
  </header>
</template>

<script>
import SearchDisk from '../sections/SearchDisk.vue'
export default {
    name:'BaseHeader',
    components:{
        SearchDisk,

    }

}
</script>

<style>
header {
    padding: 2.875rem 0;
    background-color: grey;
}
img{
    width: 100px;
    height: 100px;
}

</style>