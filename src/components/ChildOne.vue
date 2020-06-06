<template>
  <div>
    <div class="Nav d-flex">
      <div class="all hover">全部</div>
      <div class="marg-lrs">精华</div>
      <div class="marg-lrs">分享</div>
      <div class="marg-lrs">问答</div>
      <div class="marg-lrs">招聘</div>
      <div class="marg-lrs">客户端测试</div>
    </div>
    <div>
      <div v-for="(item,index) in arr" :key="index">
        <div v-if="index < 39">
          <div class="hp-item">
            <img :src="item.author.avatar_url" alt width="30"/>
            <div class="hp-item1">
              <span class="hp-item2">{{item.reply_count}}</span>
              <span class="hp-item3">/{{item.visit_count}}</span>
            </div>
            <div>
              <div v-if="item.tab==='share'">
                <div v-if="index < 2">
                  <div class="share">置顶</div>
                </div>
                <div v-else>
                  <div class="ask">分享</div>
                </div>
              </div>
              <div v-else-if="item.tab==='ask'">
                <div class="ask">问答</div>
              </div>
              <div v-else>
                <div class="share">精华</div>
              </div>
            </div>
            <div class="hp-item4">{{item.title}}</div>
          </div>
        </div>
      </div>

      <el-pagination
        @size-change="handleSizeChange"
        @current-change="handleCurrentChange"
        :current-page="currentPage4"
        :page-sizes="[10, 20, 40]"
        :page-size="4"
        layout="total, sizes, prev, pager, next, jumper"
        :total="40"
        class="el-pagination"
      ></el-pagination>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "",
  props: {},
  data() {
    return {
      currentPage1: 10,
      currentPage2: 10,
      currentPage3: 10,
      currentPage4: 10,
      arr: []
    };
  },
  components: {},
  methods: {
    handleSizeChange(val) {},
    handleCurrentChange(val) {},
    getData() {
      axios
        .get(`https://cnodejs.org/api/v1/topics`)
        .then(res => {
          this.arr = res.data.data;
        })
        .catch(err => {});
    },
    getDateTimeFormat(unixtime) {
        let currTime = Date.parse(new Date())
        console.log(currTime);
        let time = ((parseInt(currTime)/1000) - parseInt(unixtime)) 
            time = Math.abs(time);
            // 少于一分钟 
            if (time < 60) { 
                return "刚刚"; 
            } 
            // 秒转分钟 
            var minuies = time / 60; 
            if (minuies < 60) { 
                return Math.floor(minuies) + "分钟前"; 
            } 
            // 秒转小时 
            var hours = time / 3600; 
            if (hours < 24) { 
                return Math.floor(hours) + "小时前"; 
            } 
            //秒转天数 
            var days = time / 3600 / 24; 
            if (days < 30) { 
                return Math.floor(days) + "天前"; 
            } 
            //秒转月 
            var months = time / 3600 / 24 / 30; 
            if (months < 12) { 
                return Math.floor(months) + "月前"; 
            } 
            //秒转年 
            var years = time / 3600 / 24 / 30 / 12; 
            return Math.floor(years) + "年前";
        }
  },
  mounted() {
    this.getData();
  },
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.Nav {
  background: #f6f6f6;
  padding: 10px;
}
.all {
  margin: 0 10px;
  padding: 3px 4px;
  background: #80bd01;
  color: #fff;
  font-size: 14px;
  border-radius: 3px;
}
.marg-lrs {
  font-size: 14px;
  color: #80bd01;
  display: flex;
  align-items: center;
}
.marg-lrs:hover {
  color: black;
  cursor: pointer;
}
.hp-item {
  padding: 10px;
  display: flex;
  align-items: center;
  border-bottom: 1px solid #f0f0f0;
}
.hp-item1 {
  width: 70px;
  display: inline-block;
  text-align: center;
}
.hp-item2 {
  color: #9e78c0;
  font-size: 14px;
}
.hp-item3 {
  font-size: 10px;
  color: #b4b4b4;
}
.share {
  background: #80bd01;
  padding: 2px 4px;
  border-radius: 3px;
  -webkit-border-radius: 3px;
  -moz-border-radius: 3px;
  -o-border-radius: 3px;
  color: #fff;
  font-size: 12px;
}
.ask {
  background-color: #e5e5e5;
  color: #999;
  padding: 2px 4px;
  border-radius: 3px;
  -webkit-border-radius: 3px;
  -moz-border-radius: 3px;
  -o-border-radius: 3px;
  font-size: 12px;
}
.hp-item4 {
  margin-left: 5px;
}
.hp-item4:hover {
  cursor: pointer;
  text-decoration: underline;
}
.el-pagination {
  padding-left: 10px;
  padding-top: 10px;
}
</style>