<template>
 <div class="askitem">
   <ul>
       <li>
            <div class="activity fl">
                <dl>
                    <dd><p class="number">1</p><p><i class="iconfont icon-dianzan"></i></p></dd>
                    <dd><p class="number">2</p><p><i class="iconfont icon-dui2"></i></p></dd>
                    <dd><p class="number">3</p><p><i class="iconfont icon-vfa_eye"></i></p></dd>
                </dl>
            </div>
            <div class="issue-title overflow fl">
                <a href="answer.html"><h3>未来 3~5 年内，哪个方向的机器学习人才最紧缺？</h3></a>
                <div class="item">
                    <div class="item-list overflow">
                        <a href="">angular</a>
                        <a href="">typesctipt</a>
                        <a href="">icon-framework</a>
                        <a href="">iconic3</a>
                        modified 57 secs ago <font color="#2d96df">M.Hahjk</font>38
                    </div>
                </div>
            </div>
        </li>
   </ul>
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
.askitem {
  ul li {
    border-radius: 10px;
    margin-bottom: 30px;
    box-shadow: 0 4px 8px 0 rgba(7, 17, 27, 0.05);
    height: 100px;
    padding-top: 30px;
    &:hover {
      box-shadow: 0 8px 16px 0 rgba(7, 17, 27, 0.1);
    }
    .activity {
      margin-top: 10px;
      dl dd {
        float: left;
        margin-left: 10px;
        border: 1px solid transparent;
        padding: 5px 20px;
        margin-top: 0;
        &.active {
          border: 1px solid #329d78;
        }
        .number {
          font-size: 18px;
        }
        p i {
          margin-left: -5px;
        }
        .issue-title {
          margin-left: 30px;
        }
      }
    }
    .issue-title h3 {
      color: #2d96df;
      margin-top: 5px;
      text-align: left;
    }
    .item {
      margin-top: 10px;
      a {
        background: #e1ecf4;
        padding: 6px 10px;
        color: #2d96df;
        display: inline-block;
      }
    }
  }
}
</style>
