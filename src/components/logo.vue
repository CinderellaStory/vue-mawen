<template>
    <div class="logo" @click="Logo">
        <img src="../../static/images/logo.png" width="120px">
    </div>
</template>
<script>
export default {
    data(){
        return{

        }
    },
    methods:{
        Logo(){
            this.$router.push({path:"/home"})
        }
    }
}
</script>


<style scoped lang="less">
.logo {
  text-align: left;
  padding: 80px;
  cursor: pointer;
}
</style>
