<template>
    <div class="icons">
        <swiper>
            <swiper-slide v-for="(page,index) of pages" :key="index">
                <div class="icon" v-for="item of page" :key="item.id">
                    <div>
                        <img :src="item.imgUrl" alt="">
                    </div>
                    <p>{{item.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeIcons',
    data () {
        return {
                list: [
                {
                    id: '0001',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/flight.png',
                    desc: '机票'
                },{
                    id: '0002',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/hotel.png',
                    desc: '酒店'
                },{
                    id: '0003',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/piao.png',
                    desc: '景点门票'
                },{
                    id: '0004',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/train.png',
                    desc: '火车票'
                },{
                    id: '0005',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/package.png',
                    desc: '度假'
                },{
                    id: '0006',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/flight.png',
                    desc: '机票'
                },{
                    id: '0007',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/hotel.png',
                    desc: '酒店'
                },{
                    id: '0008',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/piao.png',
                    desc: '景点门票'
                },{
                    id: '0009',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/train.png',
                    desc: '火车票'
                },{
                    id: '0010',
                    imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/package.png',
                    desc: '度假'
                }
            ]
        }
    },
    computed: {
        pages () {
            const pages = []
            this.list.forEach( (item, index) => {
                const page = Math.floor(index / 8)
                if(!pages[page]){
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/style.scss';
.icons /deep/ .swiper-container{
    width: 100%;
    height: 0;
    padding-bottom: 50%;
}
.icons{
    width: 100%;
    height: 0;
    padding-bottom: 50%;
    .icon{
        width: 25%;
        height: 0;
        padding-bottom: 25%;
        float: left;
        overflow: hidden;
        >div{
            width: 90%;
            margin: 0 auto;
            padding: 0.05rem 0.15rem;
            box-sizing: border-box;
            padding-bottom: 80%;
            height: 0;
            img{
                width: 100%;
            }
        }
        >p{
            text-align: center;
            font-size: 0.26rem;
            color: $textColor;
            @include ellipsis();
            position: relative;
            @include linear-gradient($direction:right,$color1:transparent,$color2:#306eff,$color3:transparent);
            // &:after{
            //     content: '';
            //     display: block;
            //     position: absolute;
            //     @include triangle($width:.4rem,$direction:top,$color:green); 
            //     @include positionAbsolute($top:null,$right:0,$bottom:0,$left:null)
            // }
        }
    }
}
</style>