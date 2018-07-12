<template>
    <div class="logincontent mw">
        <div class="sign mb20 ov">
            <div class="fl text-one">登录</div>
            <div class="fr text-two">注册</div>
        </div>
        <form action="" method="">
            <div class="content" :model="loginForm">
                <div class="group">
                    <input type="text" placeholder="请输入手机号码或邮箱" v-model="loginForm.userName">
                    <span class="text" v-bind:class="{numbertext:isNumberText}">手机号码或邮箱不能为空</span>
                </div>
                <div class="group">
                    <input type="password" placeholder="请输入密码" v-model="loginForm.password">
                    <span class="text" v-bind:class="{passtext:isPassText}">密码不能为空</span>
                </div>
                <div class="group ov">
                    <div class="RememberText fl">
                        <input type="checkbox" name="remember" id="remember" checked class="vm">
                        <label for="remember">记住密码</label>
                    </div>
                    <router-link to='forget' class="ForgetText fr">忘记密码</router-link>
                </div>
                <div class="group">
                    <button class="btn logionbtn" @click="handleLogin('loginForm')">登录</button>
                </div>
                <div class="group">
                    <h6>
                        <i></i>
                        <span>其他方式登录</span>
                        <i></i>
                    </h6>
                </div>
                <div class="group"> 
                     <ul>
                         <li>QQ</li>
                         <li>微信</li>
                         <li>微博</li>
                     </ul>
                </div>
             </div>
        </form>
        <div class="tooltip" v-bind:class="{active:isActive}">
            <span>请输入密码长度为6~16，且必须输入数字和字母（至少一位）</span>
        </div>
        <div class="tooltip" v-bind:class="{Number:isNumber}">
            <span>请输入正确的手机号码</span>
        </div>
    </div>
</template>

<script type="text/javascript">
export default {
  data() {
    return {
        isActive:false,
        isPassText:false,
        isNumber:false,
        isNumberText:false,
        loginForm:{
            userName:"",
            password:""
        }
    }
  },
  methods:{
      handleLogin(formName){
        var name = this.loginForm.userName;
        var pass = this.loginForm.password;
        var regexp = /(?=^.*?\d)(?=^.*?[a-zA-Z])^[0-9a-zA-Z]{6,16}$/; //密码长度为6~16，且必须输入数字和字母（至少一位）
        var phonenumber=/^[1][3,4,5,7,8][0-9]{9}$/;  //手机号正则
        var r = pass.match(regexp);
        var number = name.match(phonenumber);
          if(name==""){
                this.isNumberText=true;
              return false;
          }else if(number == null){
                this.isNumber=true;
                return false;
          }else if(pass==""){
              this.isPassText=true;
              this.isNumber=false;
               return false;
          }else if(r == null){
            this.isPassText=false;
            this.isActive=true;
            this.isNumberText=false;
            this.isNumber=false;
               return false;
          }
          else{
             this.isActive=false;
             this.isNumber=false;
              return
          }
      }
  }
}
</script>

<style scoped lang="less">
@orange: #fe7300;
@red: #ea6f5a;
@grey: #666;
@lightgrey: #c3c3c3;
@blue: #59b0ff;
.login {
  .logincontent {
    width: 340px;
    background: #fff;
    padding: 30px 30px 40px;
    box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
    .sign {
      .text-one {
        color: @red;
        font-weight: bold;
        font-size: 18px;
      }
      .text-two {
        color: @orange;
      }
    }
    .content {
      .group {
        margin-bottom: 20px;
        display: block;
        input[type="text"] {
          outline: none;
          width: 94%;
          padding-left: 10px;
          height: 40px;
          border-radius: 3px;
          border: 1px solid #c3c3c3;
          &:focus{
              border: 1px solid @orange;
          }
        }
        .text{
            color: red;
            display: none;
            margin-top: 10px;
        }
        .passtext,.numbertext{
            display: block;
        }
        input[type="password"] {
          outline: none;
          width: 94%;
          padding-left: 10px;
          height: 40px;
          border-radius: 3px;
          border: 1px solid #c3c3c3;
          &:focus{
              border: 1px solid @orange;
          }
        }
        .RememberText {
          width: 80%;
          color: @grey;
        }
        .ForgetText {
          color: @lightgrey;
        }
        .logionbtn {
          width: 100%;
          background: @blue;
        }
        h6 {
            span {
            margin: 0 20px;
            color: #b5b5b5;
            font-size: 14px;
            }
            i {
            width: 30%;
            height: 1px;
            background: #b5b5b5;
            vertical-align: middle;
            display: inline-block;
            }
        }
        ul{
            li{
                float: left;
                margin-right: 60px;
                cursor: pointer;
            }
        }
      }
    }
    .tooltip{
        border: 1px solid #efefef;
        box-shadow: 1px 1px 1px #efefef;
        position: absolute; display: none;
        padding: 10px;
        background: #fff;
        border-radius: 4px;
        width: 196px;
        left: 1020px;
    }
    .active{
            display: block;
            top: 346px;
        }
        .Number{
            display: block;
            top: 290px;
        }
    }
}
</style>
