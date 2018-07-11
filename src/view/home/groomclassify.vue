<template>
 <div class="groomclassify">
    <!--推荐分类-->
    <div class="classify">
        <div class="title">
            <span>推荐分类</span>
            <i class="fr cursor">全部分类</i>
        </div>
        <div class="list">
            <ul>
                <li>
                    <div class="item overflow">
                        <div class="fl">
                            <a href="" target="_blank"><img width="38" height="38" src="http://upload.jianshu.io/users/upload_avatars/3627484/eb973bb9-37ba-4d07-acec-850c0a66d1bb.png?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96" alt="" class="locus" /></a>
                        </div>
                        <div class="fl">
                            <h6 class="name">C++</h6>
                            <p>共有123243关注</p>
                        </div>
                        <a href="" class="follow fr">关注</a>
                    </div>
                </li>
            </ul>
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
.groomclassify {
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
  .list {
    ul {
      li {
        margin-top: 30px;
        p {
          display: block;
        }
        .item p {
          color: #b7c5d6;
          margin-left: 10px;
        }
        .name {
          color: #000;
          font-weight: bold;
          text-align: left;
          margin-left: 10px;
        }
        .follow {
          width: 50px;
          height: 25px;
          line-height: 25px;
          text-align: center;
          color: #fe7300;
          border: 1px solid #e2e6e8;
          display: inline-block;
        }
      }
    }
  }
}
</style>
