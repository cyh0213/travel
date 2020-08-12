<template>
    <div class="wrapper">
        <swiper ref="mySwiper" 
                :options="swiperOptions"
                :auto-update="true"
                :auto-destroy="true"
                :delete-instance-on-destroy="true"
                :cleanup-styles-on-destroy="true"
 
        >
            <swiper-slide :key="banner.id" v-for="banner in banners">
                <img class="swiper-img" :src="banner.imgUrl" alt="">
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    neme: 'HomeBanner',
    data () {
        return {
            banners: [
                        {id: '0001',imgUrl:'https://imgs.qunarzz.com/vs_ceph_vcimg/b8c4527c41649814cc4cf86880abba54.jpeg'},
                        {id: '0002',imgUrl:'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg'},
                        {id: '0003',imgUrl:'https://imgs.qunarzz.com/vs_ceph_vcimg/c0a60fa20379efa4f02ce527a680dc1b.jpeg'}
                    ],
            swiperOptions: {
                loop: true,
                autoplay: 3000,
                effect: 'slide',
                pagination: '.swiper-pagination',
                observer: true,
                observeParents: true,
                slidesPerView: 'auto',
                // ...
            }    
        }
    },
    computed: {
      swiper() {
        return this.$refs.mySwiper.$swiper
      }
    },
    mounted() {
    //   console.log('Current Swiper instance object', this.mySwiper)
    //   this.swiper.slideTo(3, 1000, false)
    }

}
</script>

<style lang="scss" scoped>
.wrapper /deep/ .swiper-pagination-bullet-active{
    background: #fff !important;
}
.wrapper{
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 30.47%;
    .swiper-img{
        width: 100%;
    }
}
</style>