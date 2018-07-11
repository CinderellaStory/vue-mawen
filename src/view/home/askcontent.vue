// 中间内容组件包含提问组件和问题列表组件部分
<template>
 <div class="askcontent fl">
     <askbanner></askbanner>
     <askitem></askitem>
 </div>
</template>

<script type="text/javascript">
import askitem from './askitem'
import askbanner from './askbanner'

  export default {
   data() {
     return {

      }
  },
   components: {
       askitem,askbanner
   }
 }
</script>

<style scoped lang="less">


</style>
