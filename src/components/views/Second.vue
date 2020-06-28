<template>
  <div class="second-app">
    {{msg}}
    <comfirm text="注册" @message="getMessage"></comfirm>
    <p class="link">
      <router-link to="/first">去第一个页面</router-link>
    </p>
  </div>
</template>
<script>
import Comfirm from "@/components/sub/Confirm";
export default {
  name: "second-app",
  components: {
    Comfirm
  },
  data() {
    return {
      msg: "wecome to second-app"
    };
  },
  methods: {
    getMessage(val) {
      console.log(val);
    }
  }
};
</script>
<style lang="less" scoped>
.second-app {
  font-size: 30px;
  .link {
    a {
      color: #f9f;
    }
  }
}
</style>