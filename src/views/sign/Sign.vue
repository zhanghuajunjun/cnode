<template>
  <div class="f-dir-mid">
    <div class="sign">
      <div class="sign-item">
        <div class="sign-zhuye flex-a-c">
          <div class="zhuye">主页</div>
          <span class="padd-lr">/</span>
          登录
        </div>
        <div>
          <el-form
            :model="ruleForm"
            status-icon
            :rules="rules"
            ref="ruleForm"
            label-width="100px"
            class="demo-ruleForm"
          >
            <el-form-item label="用户名" prop="username">
              <el-input v-model="ruleForm.username"></el-input>
            </el-form-item>
            <el-form-item label="密码" prop="pass">
              <el-input type="password" v-model="ruleForm.pass" autocomplete="off"></el-input>
            </el-form-item>
            <el-form-item label="确认密码" prop="checkPass">
              <el-input type="password" v-model="ruleForm.checkPass" autocomplete="off"></el-input>
            </el-form-item>
            <el-form-item>
              <el-button type="primary" @click="submitForm('ruleForm')">登录/el-button>
              <el-form-item>
                <a href="https://cnodejs.org/auth/github">
                  <el-button @click="resetForm('ruleForm')">通过 GitHub 登录</el-button>
                </a>
              </el-form-item>
              <el-form-item>
                <a href="">忘记密码？</a>
              </el-form-item>
            </el-form-item>
          </el-form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {},
  data() {
    return {
      ruleForm: {
        username: '',
        pass: '',
        checkPass: '',
      },
      rules: {
        username: [],
        pass: [],
        checkPass: []
      }
    };
  },
  components: {},
  methods: {},
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.f-dir-mid {
  background: #e1e1e1;
}
.sign {
  width: 90%;
  padding: 15px 0;
}
.sign-item {
  margin-right: 305px;
  background: white;
  height: 300px;
}
.sign-zhuye {
  font-size: 14px;
  color: #999;
  background: #f6f6f6;
  padding: 10px;
}
.zhuye {
  color: #80bd01;
  font-size: 14px;
}
.padd-lr {
  color: #cccccc;
}
</style>