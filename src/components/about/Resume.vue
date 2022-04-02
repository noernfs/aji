
<template>
<div class="" style="text-align: -webkit-center">
    <div class="mb-5 text-gray-100">
        <!-- <h2 class="text-2xl md:text-4xl text-white font-bold font-sans">PROFESIONALITAS</h2> -->
    </div>
    
  <div>
  <swiper :modules="modules" :pagination="{ clickable: true }">
    <swiper-slide><img src="img/gm1.webp" alt="logo" class="h-100 md:h-45"></swiper-slide>
    <swiper-slide><img src="img/gm2.webp" alt="logo" class="h-100 md:h-45"></swiper-slide>
    <swiper-slide><img src="img/gm3.webp" alt="logo" class="h-100 md:h-45"></swiper-slide>
  </swiper>
  </div>
</div>
</template>

<script>
  import SwiperClass, { Pagination } from 'Swiper'
  import { Swiper, SwiperSlide } from 'vue-awesome-swiper'

  // import swiper module styles
  import 'swiper/css'
  import 'swiper/css/pagination'
  // more module style...

  export default {
    components: {
      Swiper,
      SwiperSlide
    },
    setup() {
      return {
        modules: [Pagination]
      }
    }
  }
</script>

<style scoped>

</style>