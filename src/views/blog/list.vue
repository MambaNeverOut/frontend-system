<template>
  <div class="">博客</div>
</template>

<script>
import { fetchList } from "@/api/blog";
export default {
  components: {},
  data() {
    return {
      blogList: [],
      count: 50
    };
  },
  created () {
    this.getList()
  },
  methods: {
    getList() {
      fetchList({
        start: this.blogList.length,
        count: this.count
      }).then(res=>{
        console.log(res);
      });
    }
  }
};
</script>

<style lang="" scoped></style>
