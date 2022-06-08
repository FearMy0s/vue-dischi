<template>
    <div class="disk">
      <img :src="disk.poster" :alt="disk.author" >
      <h5>{{disk.title}}</h5>
      <hr>
      <div>{{disk.year}}</div>
      <div>{{disk.genre}}</div>
  </div>
  
</template>

<script>
export default {
    name: 'diskCard',
    props: {
        disk: Object,
    }
}
</script>

<style lang="scss" scoped>
.disk {
    text-align: center;
    color: white;
    font-size: 20px;
    img {
        margin-top: 30px;
        max-width: 100%;
        box-shadow: 2px 2px 10px #888;
        margin-bottom: 20px;
    }
}
</style>