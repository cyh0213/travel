<template>
  <div class="home">
    <home-header></home-header>
    <home-banner></home-banner>
    <home-icons></home-icons>
  </div>
</template>

<script>
// @ is an alias to /src
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
import HomeHeader from '@/components/HomeHeader.vue'
import HomeBanner from '@/components/HomeBanner.vue'
import HomeIcons from '@/components/HomeIcons.vue'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeBanner,
    HomeIcons
  },
  directives: {
    swiper: directive
  }

}
</script>
