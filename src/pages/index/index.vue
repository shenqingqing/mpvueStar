<template>
  <div>
     <mpvue-star animate="animated bounceIn" color="#F05654">
    <!-- <mpvue-star animate="animated bounceIn" color="rgb(152, 138, 222)"> -->
        <!-- <template slot="icon"> <img  src="../../../static/img/1.png" /></template> -->
        <!-- <template slot="icon"><i  class="iconfont icon-close"></i></template> -->
         <template slot="icon"><i  class="i-star__text">❤</i></template>
    </mpvue-star>
  </div>
</template>

<script>
import MpvueStar from '@/components/MpvueStar'

export default {
  data () {
    return {
      motto: 'Hello World',
      userInfo: {}
    }
  },

  components: {
    MpvueStar
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      wx.navigateTo({ url })
    },
    clickHandle (msg, ev) {
      console.log('clickHandle:', msg, ev)
    }
  },

  created () {
    
  }
}
</script>

<style scoped>
@import '../../../static/style/main.less';
@import '../../../static/style/icon.css';
@import '../../../static/style/animate.css';


</style>
