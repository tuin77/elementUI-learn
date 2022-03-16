<template>
  <div id="app">
    <!-- <el-row>
      <el-button disabled>默认按钮</el-button>
      <el-button type="primary">主要按钮</el-button>
      <el-button type="success">成功按钮</el-button>
      <el-button type="info">信息按钮</el-button>
      <el-button type="warning">警告按钮</el-button>
      <el-button type="danger">危险按钮</el-button>
      <el-button type="text">危险按钮</el-button>
    </el-row> -->
    <el-button type="text" @click="dialogVisible = true">点击打开 Dialog</el-button>

    <el-dialog
      title="提示"
      :visible.sync="dialogVisible"
      width="30%"
      :before-close="handleClose">
      <span>这是一段信息</span>
      <span slot="footer" class="dialog-footer">
        <el-button @click="dialogVisible = false">取 消</el-button>
        <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
      </span>
    </el-dialog>

    <!-- <my-button>提 交</my-button> -->

  </div>
</template>


<script>
import ElButton from './components/button/button.vue'
import ElDialog from './components/dialog/dialog.vue'
  export default {
  name: 'App',
  components: {
    ElButton,
    ElDialog
  },
    data() {
      return {
        dialogVisible: false
      };
    },
    methods: {
      handleClose() {
        this.$confirm('确认关闭？')
          .then(() => {
            console.log();
          })
          // .catch(_ => {});
      }
    }
  };
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
