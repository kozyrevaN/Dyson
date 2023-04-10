<template>
    <swiper :slides-per-view="3"
    :space-between="50"
    parallax
    grabCursor
    observer
    observeParents
    navigation
    :pagination="{ clickable: true }"
    :scrollbar="{ draggable: true }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
    style="max-width:1920px;padding:50px 10px;"
    >
        
            <swiper-slide v-for="(tovar) in tovars" :key="tovar.id" >
                <tovar-item 
                     :tovar="tovar"
                     :key="tovar.id"
                />  
            </swiper-slide>
           
         
    </swiper>
</template>

<script>
import TovarItem from './TovarItem.vue'
import { Navigation, Pagination, Scrollbar, A11y } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';



    export default {
      components: { TovarItem, Swiper,
      SwiperSlide,},
      setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [Navigation, Pagination, Scrollbar, A11y],
      };
    },
        props:{
            tovars:{
                type:Array,
                required:true
            }

        }
    }
</script>

<style  scoped>

</style>