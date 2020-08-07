<template>
  <div class="home">
    <home-header></home-header>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeHeader from '@/components/HomeHeader.vue'

export default {
  name: 'Home',
  components: {
    HomeHeader
  }
}
</script>
