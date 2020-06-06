<template>
  <div class="f-dir-mid">
    <div class="sign flex-j-sb">
      <div class="sign-item">
        <div class="sign-zhuye flex-a-c">
          <div class="homepage hover" @click="homePage">主页</div>
          <span class="padd-lr">/</span>
          登录
        </div>
        <div class="login">
          <el-form
            :model="ruleForm"
            status-icon
            :rules="rules"
            ref="ruleForm"
            label-width="100px"
            class="demo-ruleForm"
          >
            <el-form-item label='用户名' prop="username">
              <el-input v-model="ruleForm.username" class="eipt"></el-input>
            </el-form-item>
            <el-form-item label="密码" prop="pass">
              <el-input type="password" v-model="ruleForm.pass" class="eipt"></el-input>
            </el-form-item>
            <el-form-item label="确认密码" prop="checkPass">
              <el-input type="password" v-model="ruleForm.checkPass" class="eipt"></el-input>
            </el-form-item>
            <el-form-item>
              <el-button type="primary" @click="submitForm('ruleForm')">登录</el-button>
              <el-button type="primary" class="github">通过 GitHub 登录</el-button>
              <el-button @click="resetForm('ruleForm')">重置</el-button>
              <a href="##">忘记密码？</a>
            </el-form-item>
          </el-form>
        </div>
      </div>
      <div class="about">
        <div class="ab-top">关于</div>
        <div class="ab-item">
          <p class="ab-item1">CNode：Node.js专业中文社区</p>
          <p class="ab-item1">在这里你可以：</p>
          <ul>
            <li class="item3">和其它人一起进步</li>
            <li class="item3">向别人提出你遇到的问题</li>
            <li class="item3">帮助遇到问题的人</li>
            <li class="item3">分享自己的知识</li>
          </ul>
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
    let validatePass = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("请再次输入密码"));
      } else if (value !== this.ruleForm.pass) {
        callback(new Error("两次输入密码不一致!"));
      } else {
        callback();
      }
    };
    return {
      ruleForm: {
        username: "",
        pass: "",
        checkPass: ""
      },
      rules: {
        username: [
          { required: true, message: "用户名不能为空", trigger: "blur" },
          { min: 5, max: 10, message: "用户名在5-10位之间", trigger: "blur" }
        ],
        pass: [
          { required: true, message: "密码不能为空", trigger: "blur" },
          { min: 6, max: 18, message: "密码在6-18位之间", trigger: "blur" }
        ],
        checkPass: [{ required: true, validator: validatePass, trigger: "blur" }]
      }
    };
  },
  components: {},
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate(valid => {
        if (valid) {
          alert("登录成功");
          this.$router.push('/')
        } else {
          alerta("账号或密码错误");
          return false;
        }
      });
    },
    resetForm(formName) {
      this.$refs[formName].resetFields();
    },
    homePage(){
      this.$router.push('/')
    }
  },
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
  background: white;
  padding-bottom: 40px;
  width: 1065px;
}
.sign-zhuye {
  font-size: 14px;
  color: #999;
  background: #f6f6f6;
  padding: 10px;
}
.homepage {
  color: #80bd01;
  font-size: 14px;
}
.padd-lr {
  color: #cccccc;
}
.login {
  margin-left: 50px;
  margin-top: 40px;
}
a {
  padding: 0 10px;
  text-decoration: none;
}
.eipt {
 width: 300px;
}
.about {
  width: 290px;
}
.ab-top {
  font-size: 14px;
  background: #f6f6f6;
  padding: 10px;
}
.ab-item {
  background: white;
  padding: 10px;
}
.ab-item1{
  font-size: 14px;
  margin-bottom: 10px;
}
.ab-item2{
  padding-left: 10px;
  font-size: 13px;
}
ul {
  padding-left: 20px;
  font-size: 13px;
}
.item3 {
  padding: 5px 0;
  
}
.github {
  background-color: #5bc0de;
}
.github:hover {
  background-color: #6396b4;
}
</style>