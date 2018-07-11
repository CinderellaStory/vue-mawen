<template>
    <div class="askbanner">
        <span>程序员专用的问答社区</span>
        <router-link to="/ask" class="btn fr">我要提问</router-link>
    </div>
</template>

<script type="text/javascript">
export default {
  data() {
    return {};
  },
  components: {}
};
</script>

<style scoped lang="less">
.askbanner {
  margin-bottom: 20px;
  border-radius: 10px;
  background: url(../../../static/images/ask-banner.png) no-repeat center center;
  width: 800px;
  height: 100px;
  span {
    color: #fff;
    font-size: 40px;
    line-height: 100px;
    margin-left: 20px;
  }
  a {
    margin-right: 30px;
    margin-top: 30px;
    border-radius: 5px;
    background: #fe7300;
    padding: 6px 20px;
    text-align: center;
    color: #fff;
    font-size: 16px;
  }
}
</style>
