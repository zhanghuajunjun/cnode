<template>
 <div>
   <div class="box flex-j-c">
      <div class="box1">
        <div class=" d-flex">
          <div class="head hover">
            <img src="https://static2.cnodejs.org/public/images/cnodejs_light.svg" width="120" />
          </div>
          <form action="/search" class="pos-re sousuo">
            <i class="iconfont icon-sousuo"></i>
            <input type="text" class="ipt" />
          </form>
        </div>
        <div class=" d-flex">
          <div class="head-item">首页</div>
          <div class="head-item">新手入门</div>
          <div class="head-item">API</div>
          <div class="head-item">关于</div>
          <div class="head-item">注册</div>
          <div class="head-item" @click="ClickSign">登录</div>
        </div>
      </div>
    </div>
 </div>
</template>

<script>
 export default {
   name: '',
   props: {

   },
   data () {
     return {

     }
   },
   components: {

   },
   methods: {
     ClickSign(){
       
     }
   },
   mounted() {

   },
   watch: {

   },
   computed: {

   }
 }
</script>

<style scoped lang='scss'>
.box {
  width: 100%;
  background: #444;
  padding: 5px 0;
}
.box1 {
  width: 90%;
  display: flex;
  justify-content: space-between;
}
.icon-sousuo {
  position: absolute;
  left: 5px;
  top: 8px;
  color: #666;
  font-weight: 700;
  font-size: 14px;
}
.sousuo {
  margin-top: 6px;
  height: 28px;
}
.head-item {
  font-size: 13px;
  color: #cccccc;
  padding: 10px 15px;
}
.head-item:hover {
  cursor: pointer;
  color: #fff;
}
</style>