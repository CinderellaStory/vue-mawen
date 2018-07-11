<template>
  <div class="mheader">
     <div class="mw">
       <div class="logo"><img src="../../static/images/logo.png"></div>
        <div class="navbar">
          <ul>
            <router-link v-for="(item,index) in items" :to="item.to" :key="index" tag="li">
                {{item.text}}
            </router-link>
          </ul>
        </div>
        <div class="search fl mr10">
          <input type="text" placeholder="请输入搜索内容">
        </div>
        <button class="btn askbtn fl">我要提问</button>
        <div class="btn-group fr">
          <button class="btn loginbtn fl mr10">登录</button>
          <button class="btn registerbtn fl">注册</button>
        </div>
     </div>
  </div>
</template>

<script>
export default {
  name: 'mheader',
  data () {
    return {
      items:[
        {text:'搜索',to:''},
        {text:'问题详情页',to:''},
        {text:'联系我们',to:''},
        {text:'名人榜',to:''}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
button{
  border: 0;
}
.mheader{
  height: 90px;
  background: #303643;
  line-height: 90px;
    .logo{
      float: left;
      margin-right: 50px;
      img{
        width: 80px;
        vertical-align: middle;
      }
    }
    .navbar{
      ul{
        float: left;
        li{
          float: left;
          margin-right: 50px;
          color: #fff;
          text-align: center;
          cursor: pointer;
        }
      }
    }
    .search{
      input{
          padding-left: 15px;
          outline: none;
          height: 34px;
          border: 1px solid #999;
          width: 280px;
          border-radius: 5px;
      }
    }
    .btn{
        &.askbtn{
        border: 1px solid #0f88eb;
        background: #0f88eb;
        }
        &.loginbtn{
            background: #59b0ff;
        }
        &.registerbtn{
          background: #5bbf5a;
        }
    }
    .btn-group{

    }
}
</style>
