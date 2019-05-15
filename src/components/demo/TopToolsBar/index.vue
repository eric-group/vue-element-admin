<template>
  <div :class="device!=='mobile' ? 'wapperPC' : 'wapperMobile' ">
    <el-button>aaa</el-button>
    <el-button>bbb</el-button>
    <el-button>ccc</el-button>
    <el-button>ddd</el-button>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  computed: {
    ...mapGetters([
      'device'
    ])
  }
}
</script>

<style scoped>
  .wapperPC {
    width: calc(100% - 16rem);
    height: 100%;
    margin-left: 3rem;
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .wapperMobile {
    width: calc(100% - 8rem);
    height: 100%;
    margin-left: 3rem;
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
