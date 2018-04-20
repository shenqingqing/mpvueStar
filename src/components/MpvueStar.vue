<template>
  <div class="mpVueStar">
    <div class="mpVue_ground">
        <div class="mpvue_icon" @click="toggle" :class="animateClass" :style='{ color: colorValue }'>
          <slot name="icon"></slot>
        </div>
        <div class="mpVue_decoration" :class="{'mpVue_decoration--active':active}"></div>
    </div>
  </div>
</template>

<script>
import { isColors } from '../utils/colorRE.js'
export default {
  name: 'MpvueStar',
  props: {
    animate: String,
    color: String
  },
  methods: {
    toggle () {
      this.active = !this.active
      this.toggleAnimate = !this.toggleAnimate
      this.toggleColor = !this.toggleColor
    }
  },
  data () {
    return {
      active: false,
      toggleAnimate: false,
      toggleColor: false
    }
  },
  computed: {
    animateClass () {
      return this.toggleAnimate ? this.animate : ''
    },
    colorValue () {
      return this.toggleColor ? this.color : ''
    }
  },
  mounted () {
     if (this.color && !isColors(this.color)) {
      console.error('this color prop must be hex or rgb pattern  ---VueStarPlus')
    }
  }
}
</script>

<style>
@import '../../static/style/main.less';
@import '../../static/style/icon.css';
@import '../../static/style/animate.css';
</style>
