<template>
 <div class="fllowclassify">
    <!--我关注的分类-->
    <div class="follow-classify ov">
        <div class="title">
            <span>我关注的分类<i class="fr cursor">+</i></span>
        </div>
        <div class="follow-list ov">
            <a href="">大数据</a>
            <a href="">大数据</a>
            <a href="">大数据</a>
            <a href="">大数据</a>
            <a href="">大数据</a>
            <a href="">大数据</a>
        </div>
    </div>
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
.fllowclassify {
  .title {
    text-align: left;
    border-bottom: 1px solid #e7eaeb;
    padding-bottom: 20px;
    span {
      font-size: 16px;
      color: #14191e;
      i {
        font-size: 24px;
      }
    }
    i {
      font-size: 14px;
      font-style: normal;
      color: #9a9ea1;
      &:hover {
        color: red;
      }
    }
  }
  .follow-list {
    margin-top: 5px;
    margin-bottom: 30px;
    a {
      float: left;
      border: 1px solid #e2e6e8;
      margin-top: 5px;
      margin-left: 6px;
      padding: 5px 10px;
      color: #b2b2b1;
      &:hover {
        color: #fe7300;
      }
    }
  }
}
</style>
