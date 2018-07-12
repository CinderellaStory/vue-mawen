<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
body {
  background: #f8f8f8;
}
* {
  padding: 0;
  margin: 0;
  font-size: 14px;
}
.cursor {
  cursor: pointer;
}
.vm{ vertical-align: middle ; }
.fl {
  float: left;
}
.fr {
  float: right;
}
.ov {
  overflow: hidden;
}
.mr10 {
  margin-right: 10px;
}
.mb20 {
  margin-bottom: 20px;
}
ul {
  list-style: none;
}
#app {
}
a {
  text-decoration: none;
}
.mw {
  width: 1200px;
  margin: 0 auto;
}
.btn {
  border-radius: 5px;
  padding: 9px 14px;
  color: #fff;
  margin-top: 28px;
  cursor: pointer;
}
button{
  border: 0;
}
</style>
