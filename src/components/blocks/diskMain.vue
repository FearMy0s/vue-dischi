<template>
<main>
    <sectionDisk />
    
</main>
  
</template>

<script>
import sectionDisk from '../sections/sectionDisk.vue'

export default {
  components: { sectionDisk },
    name: 'BaseMain',

}
</script>

<style>
main{
  background-color: black;
}

</style>