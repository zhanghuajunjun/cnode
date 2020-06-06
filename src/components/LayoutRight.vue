<template>
  <div>
    <div class="right-sign">
      <p class="r-sign-item">CNode：Node.js专业中文社区</p>
      <div>
        您可以
        <a href>登录</a>或
        <a href>注册</a>,也可以
        <br />
        <div class="github">通过 GitHub 登录</div>
      </div>
    </div>
    <div class="right-picture">
      <img src="https://static.cnodejs.org/Fn4D6BhOTz1IswvmzeZ1q7QW1ls_" class=" hover" width="270" />
      <img src="https://static.cnodejs.org/FlajCCXkxZaOsuWp3k0iaiqfrJaS" class="img hover" width="270" />
      <img src="https://static.cnodejs.org/FgIok2ZlDer2QOb8sJ20S9Y8T2Jq" class=" hover" width="270" />
    </div>
    <div class="right-topic">
      <div class="right-topic-top">无人回复的话题</div>
      <div class="right-topic-item">
        <p class="hover">这个字有点难打，就不打了</p>
        <p class="marg-tbs hover">这个字有点难打，就不打了</p>
        <p class="hover">这个字有点难打，就不打了</p>
        <p class="marg-tbs hover">这个字有点难打，就不打了</p>
        <p class="hover">这个字有点难打，就不打了</p>
        <p class="marg-tops hover">这个字有点难打，就不打了</p>
      </div>
    </div>
    <div class="right-integral">
      <div class="right-integral-top">积分榜 TOP 100 >></div>
      <div class="right-integral-item">
        <p>
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p class="marg-tbs">
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p>
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p class="marg-tbs">
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p>
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p class="marg-tbs">
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p>
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p class="marg-tbs">
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p>
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
        <p class="marg-tops">
          2250
          <span class="hover1">zhanghuajun</span>
        </p>
      </div>
    </div>
    <div class="right-community">
      <div class="right-community-top">友情社区</div>
      <div class="right-community-item">
        <a href="##">
          <img src="https://static2.cnodejs.org/public/images/ruby-china-20150529.png" width="150" />
        </a>
        <div class="none"></div>
        <a href="##">
          <img src="https://static2.cnodejs.org/public/images/phphub-logo.png" width="150" />
        </a>
      </div>
    </div>
    <div class="right-QR">
      <div class="right-QR-top">
        客户端二维码
      </div>
      <div class="right-QR-item f-dir-mid">
        <img src="https://static.cnodejs.org/FtG0YVgQ6iginiLpf9W4_ShjiLfU" alt="" width="200">
        <a href="##" class="yuma">客户端源码</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {},
  data() {
    return {};
  },
  components: {},
  methods: {},
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.right-sign {
  width: 270px;
  padding: 10px;
  background: white;
  margin-bottom: 10px;
}
.r-sign-item {
  font-size: 14px;
  margin-bottom: 10px;
}
a {
  padding: 0 5px;
  text-decoration: none;
}
.github {
  display: inline-block;
  float: none;
  padding: 3px 10px;
  border: none;
  margin: 0;
  font-size: 14px;
  transition: all 0.2s ease-in-out;
  cursor: pointer;
  letter-spacing: 2px;
  border-radius: 3px;
  line-height: 2em;
  vertical-align: middle;
  color: #fff;
  background-color: #5bc0de;
  margin-top: 5px;
}
.github:hover {
  background-color: #6396b4;
}
.right-picture {
  width: 270px;
  padding: 10px;
  background: white;
  margin-bottom: 10px;
}
.img {
  margin: 10px 0;
}
.right-topic {
  width: 290px;
  background: white;
  margin-bottom: 10px;
}
.right-topic-top {
  background: #f6f6f6;
  font-size: 13px;
  padding: 10px;
}
.right-topic-item {
  padding: 10px;
  font-size: 14px;
  color: #778087;
}
.right-integral {
  width: 290px;
  background: white;
  margin-bottom: 10px;
}
.right-integral-top {
  background: #f6f6f6;
  font-size: 13px;
  padding: 10px;
}
.right-integral-item {
  padding: 10px;
  font-size: 14px;
  color: #778087;
}
.right-community {
  width: 290px;
  background: white;
  margin-bottom: 10px;
}
.right-community-top {
  background: #f6f6f6;
  font-size: 13px;
  padding: 10px;
}
.right-community-item {
  padding: 10px;
}
.none {
  height: 10px;
}
.right-QR {
  width: 290px;
  background: white;
}
.right-QR-top {
  background: #f6f6f6;
  font-size: 13px;
  padding: 10px;
}
.right-QR-item {
  padding: 10px;
}
.yuma {
  color: #778087;
  font-size: 13px;
  padding-top: 10px;
}
</style>