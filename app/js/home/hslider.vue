<template lang="html">
    <article >
      <Slider :items="items" :cname="$style.slider"/>
      <section :class="$style.list">
        <div :class="$style.item" v-for="(item,index) in enters" :key="index">
            <router-link :to="{name:item.href}">
                <img :src="item.img" :alt="item.title">
                <h4>{{item.title}}</h4>
            </router-link>
        </div>
      </section>
    </article>
</template>

<script>
import Slider from '../core/slider.vue'
export default {
    data() {
        return {
            items: [
                {
                    href:"home",
                    src:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=123&height=123"
                },
                {
                    href:"home",
                    src:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=123&height=123"
                },
                {
                    href:"home",
                    src:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=123&height=123"
                }
            ],
            enters:[{
                href:"home",
                img:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=123&height=123",
                title:"优惠"
            },
            {
                href:"home",
                img:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=123&height=123",
                title:"红包"
            },
            {
                href:"home",
                img:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=123&height=123",
                title:"抢钢镚"
            },
            {
                href:"home",
                img:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=123&height=123",
                title:"领京豆"
            },
            {
                href:"home",
                img:"//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=123&height=123",
                title:"白条"
            }
            ]
        }
    },
    components: {
        Slider
    }
}
</script>
<style lang="scss" module>
@import "../../css/element.scss";
.slider{
    margin-top:120px;
}
.list{
    @include list(row);
    background: #fff;
    padding-top: 40px;
    padding-bottom:20px;
    justify-content:space-around;
    a{
        text-decoration:none;
    }
    .item{
        text-align:center;
        img{
            display:inline-block;
            width:90px;
            height:90px;
        }
        h4{
            
            margin-top:12px;
            font-size:26px;
            color:#666;
        }
    }
}
</style>
