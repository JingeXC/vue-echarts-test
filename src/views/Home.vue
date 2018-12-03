<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <ve-line :data="chartData"></ve-line>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
// https://github.com/ElemeFE/v-charts/blob/master/README_CN.md
import VeLine from 'v-charts/lib/line.common';

export default {
  name: 'home',
  components: {
    HelloWorld,
    VeLine,
  },
  data() {
    return {
      chartData: {
        columns: ['日期', '销售量'],
        rows: [
          { '日期': '1月1日', '销售量': 123 },
          { '日期': '1月2日', '销售量': 1223 },
          { '日期': '1月3日', '销售量': 2123 },
          { '日期': '1月4日', '销售量': 4123 },
          { '日期': '1月5日', '销售量': 3123 },
          { '日期': '1月6日', '销售量': 7123 },
        ],
      },
    };
  },
};
</script>
