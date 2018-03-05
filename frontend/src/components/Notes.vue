<template>
  <div>
    <el-row>
      <el-col  style="background: #99a9bf;" :span="4">
        <el-button type="primary" round><i class="el-icon-plus"></i> 创建文档</el-button>
        <el-tree :data="notesFolder" :props="defaultProps" @node-click="handleNodeClick"></el-tree>
        <br />
      </el-col>
      <el-col :span="4">
        <el-button><i class="el-icon-back"></i></el-button>
        <el-input
          placeholder="请输入内容"
          v-model="searchContent"
          clearable>
        </el-input>
        <el-card>
          <h5>Vue租金组件使用</h5>
          <p>tttttttttttttttttttttttttttt</p>
        </el-card>
        <el-card>
          <h5>Vue租金组件使用</h5>
          <p>tttttttttttttttttttttttttttt</p>
        </el-card>
      </el-col>
      <el-col :span="16">
        <div>
          
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import Vue from 'vue';

import Button from 'element-ui';
import Col from 'element-ui';
import Row from 'element-ui';
import Tree from 'element-ui';

Vue.use(Button);
Vue.use(Col);
Vue.use(Row);
Vue.use(Tree);

export default {
  name: "notes",
  data() {
    return {
      searchContent: "",
      notesFolder: [{
        label: "分享文档",
        children: []
      }, {
        label: "我的文件夹",
        children: []
      }, {
        label: "我的分享",
        children: []
      }, {
        label: "我的标签",
        children: []
      }, {
        label: "回收站",
        children: []
      }],
      defaultProps: {
        children: 'children',
        label: 'label'
      }
    };
  },
  methods: {
    handleNodeClick(data) {
      console.log(data);
    }
  }
}
</script>

<style scoped>

</style>
