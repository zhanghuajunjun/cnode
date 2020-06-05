<template>
  <div>
    <div>
      <layout-head></layout-head>
    </div>
    <div>
      <router-view></router-view>
    </div>
    <div>
      <layout-right></layout-right>
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
</style>