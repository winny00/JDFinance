<template lang="html">
    <section :class="cname">
        <swiper :options="options" :not-next-tick="option.notNextTick">
            <swiper-slide v-for="(item,key) in items" :key="item.href">
                <router-link :to="{name:item.href}">
                    <img :src="item.src" alt="pic">
                </router-link>
            </swiper-slide>
            <div class="swiper-pagination" v-if="options.pagination"></div>
        </swiper>
    </section>
</template>
<script>
    import {swiper,swiperSlide} from "vue-awesome-swoper"
    export default {
        poprs: {
            options: {
                type: Object,
                default(){
                    return {
                        autoplay: true,
                        loop: true,
                        pagination: {
                            el:'.swiper-pagination',
                        },
                        notNextTick: false
                    }
                }
            },
            cname: {
                type: String,
                default:""
            },
            items:{
                type:Array,
                default() {
                    return []
                }
            }
        },
        data() {
            return {

            }
        },
        commonents: {
            swiper,
            swiperSlide,
        }
    }
</script>
<style lang="scss">
@import "~swiper/dist/css/swiper.css";

</style>