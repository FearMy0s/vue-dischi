<template>
    <div class="disk">
      <img :src="disk.poster" :alt="disk.author" >
      <h5>{{disk.title}}</h5>
      <hr>
      <div>{{disk.year}}</div>
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
    img {
        max-width: 100%;
        box-shadow: 2px 2px 10px #888;
        margin-bottom: 20px;
    }
    hr {
        max-width: 50px;
        margin: 1rem auto;
        opacity: 1;
    }
}
</style>