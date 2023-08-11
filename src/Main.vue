<script>
import PartComp from '@/component/Part.vue'
export default {
  name: 'MainComp',
  // 局部注册
  components: {
    'PartCom':PartComp
  },
  setup() {}
}
</script>
<template>
  <!-- <child-comp></child-comp> -->
  <part-com msg="hello world"></part-com>
  <el-button>这是elementui提供的</el-button>
</template>