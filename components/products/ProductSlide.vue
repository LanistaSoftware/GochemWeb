<template>
  <carousel
    :per-page-custom="[[200, 3], [1024, 3]]"
    :navigation-enabled="true"
    :navigation-next-label="nexticon"
    :navigation-click-target-size="2"
    :pagination-enabled="false"
  >
    <slide v-for="(slide,index) in 5" :key="index">
      Slide 1 Content
    </slide>
  </carousel>
</template>
<script>
import { Carousel, Slide } from 'vue-carousel'
export default {
  components: { Carousel, Slide },
  data () {
    return {
      nexticon: '<span class="next" style="color:red">Geç</span>'
    }
  }
}
</script>
<style lang="less" scoped>
.slider{
   background-color:rgba(0, 0, 0, 0);
   border: none;
   text-align: center;
    height: 20rem;
    opacity: 0.5;
}
.VueCarousel-navigation-prev{
    color: red !important;
}
</style>
