<template>
  <div class="footer flex-j-c">
    <div class="footer-box">
      <div class="footer-item flex-a-c">
        RSS
        <span>|</span>
        源码地址
      </div>
      <div class="f-item">
        <p class="marg-bos">CNode 社区为国内最专业的 Node.js 开源技术社区，致力于 Node.js 的技术研究。</p>
        <p>
          服务器赞助商为
          <a
            href="http://www.ucloud.cn/?utm_source=zanzhu&amp;utm_campaign=cnodejs&amp;utm_medium=display&amp;utm_content=yejiao&amp;ytag=cnodejs_logo"
          >
            <img src="https://static.cnodejs.org/FuIpEaM9bvsZKnQ3QfPtBHWQmLM9" width="92" />
          </a>
          ，存储赞助商为
          <a href="http://www.qiniu.com/?ref=cnode">
            <img
              src="https://static.cnodejs.org/Fg0jtDIcTqVC049oVu5-sn6Om4NX"
              alt="牛云存储"
              width="115"
            />
          </a>
          ，由
          <a href="https://www.aliyun.com/product/nodejs?ref=cnode">
            <img
              src="https://static.cnodejs.org/FpMZk31PDyxkC8yStmMQL4XroaGD"
              alt
              width="166"
              height="54"
            />
          </a>
          提供性能服务。
        </p>
      </div>
      <div class="f-item">
        新手搭建 Node.js 服务器，推荐使用无需备案的
        <a
          href="https://www.digitalocean.com/?refcode=eba02656eeb3" 
          class="a"
        >DigitalOcean(https://www.digitalocean.com/)</a>
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
.footer {
  background: #fff;
  position: relative;
  bottom: 0;
}
.footer-box {
  width: 90%;
  padding: 20px 0;
  color: #e2e2e2;
}
.footer-item {
  font-size: 13px;
  color: #666;
  height: 26px;
}
span {
  padding: 0 5px;
  color: #e2e2e2;
}
.f-item {
  font-size: 14px;
  color: #ababab;
  margin-bottom: 10px;
}
a {
  color: #0088cc;
  text-decoration: none;
}
</style>