<template>
  <div class="containers">
    <div>
      <layout-head></layout-head>
    </div>
    <div class="flex-j-c">
      <div class="flex-j-sb">
        <div class="home">
          <router-view></router-view>
        </div>
        <div>
          <layout-right></layout-right>
        </div>
      </div>
    </div>
    <div>
      <layout-footer></layout-footer>
    </div>
  </div>
</template>

<script>
import LayoutHead from "../../components/LayoutHead";
import LayoutFooter from "../../components/LayoutFooter";
import LayoutRight from "../../components/LayoutRight";
export default {
  name: "",
  props: {},
  data() {
    return {};
  },
  components: {
    LayoutHead,
    LayoutFooter,
    LayoutRight
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.containers {
  background: #e1e1e1;
}
.flex-j-sb {
  width: 90%;
  padding: 10px 0;
}
.home {
  width: 1065px;
  background: white;
  padding-bottom: 10px;
}
</style>