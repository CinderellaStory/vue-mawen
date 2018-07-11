<template>
 <div class="askaside fr">
    <fllowclassify></fllowclassify>
    <groomclassify></groomclassify>
 </div>
</template>

<script type="text/javascript">
import groomclassify from './groomclassify'
import fllowclassify from './fllowclassify'

  export default {
   data() {
     return {

      }
  },
   components: {
       fllowclassify,groomclassify
   }
 }
</script>

<style scoped lang="less">
.askaside{
    width: 340px;
}

</style>
