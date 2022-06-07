<template>
  <section>
      <div class="container">
          <div class="row">
              <diskCard class="col-12 col-sm-6 col-lg-3 mb-3" v-for="(disk, index) in disks" :key="index" :disk="disk"/>
          </div>
      </div>
  </section>
</template>

<script>
import diskCard from '../commons/diskCard.vue';
import axios from 'axios';
export default {
    name: 'sectionDisk',
    components: {
        diskCard,

    },
    data() {
        return {
            disks: [],
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
             .then((response) => {
            this.disks = response.data.response;
            console.log(this.disks)
        })
        .catch((error) => {
            console.log(error);
        });
    }
}
</script>

<style>

</style>