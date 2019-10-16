<template>
  <div class="navbar">
    <div class="info">
      <span class="logo">FreeTechDocHub</span>
      <span class="about" @click='dialogVisible = true'>关于作者</span>
    </div>
    <el-dialog title="关于本项目" :visible.sync="dialogVisible" width="35%">
      <!-- /* P.S. 当使用_blank时有一个容易忽略的安全漏洞，需要注意：https://developers.google.com/web/tools/lighthouse/audits/noopener?hl=zh-cn */ -->
      <div class='inside-dialog'>
        <p>
          作者：
          Swordrada
        </p>
        <div>
          <p>技术栈：</p>
          <ul>
            <li>Vue</li>
            <li>Vue Router</li>
            <li>ElementUI</li>
            <li>Axios</li>
          </ul>
        </div>
      </div>
      <span slot="footer" class="dialog-footer">
          <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
        </span>
    </el-dialog>
  </div>
</template>

<script>
  export default {
    name: "Navbar",
    data() {
      return {
        dialogVisible: false
      };
    }
  };
</script>

<style scoped lang="scss">
.navbar {
  width: 100%;
  height: 100px;
  background: #999;
  border-radius:10px;
  > div.info {
    width: 1350px;
    height: 100%;
    margin: auto;
    .logo {
      float: left;
      height: 120px;
      line-height: 90px;
      color: #fff;
      cursor: pointer;
      font-size: 25px;
      font-weight: bold;
    }
    .about {
      float: right;
      height: 120px;
      padding-left: 20px;
      line-height: 90px;
      color: #fff;
      cursor: pointer;
      font-size: 25px;
      font-weight: bold;
    }
  }
}

</style>

<style lang='scss'>
  .navbar {
    .el-dialog__body {
      padding-top: 10px;
      padding-bottom: 0;
      .inside-dialog {
        p {
          margin: auto;
        }
        .el-icon-star-off::before {
          color: #eb2f96;
        }
      }
    }
  }
</style>