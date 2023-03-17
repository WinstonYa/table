<template>
  <div>
    <Search />
    <template v-if="indexData">
      <el-table :data="tableData" style="width: 100%">
        <el-table-column prop="date" label="日期" width="180">
        </el-table-column>
        <el-table-column prop="name" label="姓名" width="180">
        </el-table-column>
        <el-table-column prop="address" label="地址"> </el-table-column>
      </el-table>
    </template>
  </div>
</template>

<script lang="ts">
import { mapState } from 'vuex';
import Slider from '@/components/slider/index.vue';
import Rectangle from '@/components/rectangle/index.vue';
import Search from '@/components/search/index.vue';

export default {
  components: {
    Slider,
    Rectangle,
    Search,
  },

  data() {
    return {
      tableData: [
        {
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄',
        },
        {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄',
        },
        {
          date: '2016-05-01',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1519 弄',
        },
        {
          date: '2016-05-03',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1516 弄',
        },
      ],
    };
  },
  computed: {
    ...mapState({
      indexData: (state) => state.indexStore?.data,
    }),
  },
};
</script>

<style></style>
