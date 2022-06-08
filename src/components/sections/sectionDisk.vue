<template>
  <section>
      <div class="container">
          <div class="row">
              <diskCard class="col-12 col-sm-6 col-lg-3 mb-3" v-for="(disk, index) in DiskFilter" :key="index" :disk="disk"/>
          </div>
      </div>
  </section>
</template>

<script>
import diskCard from '../commons/diskCard.vue';
import axios from 'axios';
import Chose from "../commons/Chose";
export default {
    name: 'sectionDisk',
    components: {
        diskCard,

    },
    data() {
        return {
            disks: [],
            Chose
        };
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
    },
    computed: {
        DiskFilter() {
            return this.disks.filter(disk => disk.genre === this.Chose.picked || this.Chose.picked === "All");
        }
    }
}
</script>

<style>

</style>