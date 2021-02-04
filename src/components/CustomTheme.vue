<template>
  <div class="app-root" :class="[themeClass, fontsizes]">
    <div class="app-container">
      <!-- header -->
      <header class="hd">
        <div class="menu"><i class="icon-liebiao"></i></div>
        <div class="txt">{{ msg }}</div>
        <div class="more"><i class="icon-caozuo"></i></div>
      </header>
      <!-- main -->
      <main class="content">
        <!-- select -->
        <div class="sel-box">
          <select v-model="color">
            <option class="cell" value="black">黑色</option>
            <option class="cell" value="red">红色</option>
            <option class="cell" value="green">绿色</option>
            <option class="cell" value="blue">蓝色</option>
            <option class="cell" value="orange">橙色</option>
            <option class="cell" value="purple">紫色</option>
          </select>
          <select v-model="fontsize">
            <option class="cell" value="small">小号</option>
            <option class="cell" value="middle">中号</option>
            <option class="cell" value="big">大号</option>
          </select>
        </div>
        <!-- banner -->
        <div class="banner"></div>
        <!-- icon -->
        <nav class="nav-box">
          <a class="item" v-for="item in books" :key="item.name">
            <i :class="item.icn"></i>
            <span>{{ item.name }}</span>
          </a>
        </nav>
      </main>
      <!-- footer -->
      <footer class="ft">
        <a class="flex" v-for="item in flexs" :key="item.name">
          <i :class="item.icn"></i>
          <span>{{ item.name }}</span>
        </a>
      </footer>
    </div>
  </div>
</template>

<script>
import "./../style/index.scss";
export default {
  name: "CustomTheme",
  data() {
    return {
      msg: "自定义主题字号",
      color: "black",
      fontsize: "middle",
      show: true,
      books: [
        { icn: "icon-beixin_2", name: "背心" },
        { icn: "icon-gaogenxie_1", name: "高跟鞋" },
        { icn: "icon-Txu_2", name: "T恤" },
        { icn: "icon-beibao_1", name: "背包" },
        { icn: "icon-banxie_1", name: "鞋子" },
        { icn: "icon-weiyi_2", name: "卫衣" },
        { icn: "icon-lianyiqun_2", name: "连衣裙" },
        { icn: "icon-fengyi_1", name: "风衣" },
        { icn: "icon-chaoduanqun", name: "超短裙" },
      ],
      flexs: [
        { icn: "icon-zhanghu", name: "账户" },
        { icn: "icon-fenlei", name: "分类" },
        { icn: "icon-gouwuche", name: "购物车" },
        { icn: "icon-wode", name: "我的" },
      ],
    };
  },
  computed: {
    themeClass() {
      return `theme-${this.color}`;
    },
    fontsizes() {
      return `font-${this.fontsize}`;
    },
  },
  methods: {
    handleClick: function () {
      this.show = !this.show;
    },
  },
};
</script>

<style scoped lang='sass'>
</style>
