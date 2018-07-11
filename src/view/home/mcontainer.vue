// 内容组件包含中间内容和侧边推送消息部分
<template>
 <div class="mcontainer mw">
     <askcontent></askcontent>
     <askaside></askaside>
 </div>
</template>

<script type="text/javascript">
import askcontent from './askcontent'
import askaside from './askaside'

  export default {
   data() {
     return {

      }
  },
   components: {
       askcontent,askaside
   }
 }
</script>

<style scoped lang="less">
.mcontainer{
    margin-top: 50px;
}
</style>
