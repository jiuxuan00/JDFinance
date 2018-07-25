<template>
  <div :class="cname">
      <swiper :options="options" :not-next-tick="options.notNextTick">
          <swiper-slide v-for="(item,index) in items" :key="index">
              <router-link :to="{name:item.href}">
                  <img :src="item.src" alt="" srcset="">
              </router-link>
          </swiper-slide>
          <div class="swiper-pagination" v-if="options.pagination" slot="pagination"></div>
      </swiper>
  </div>
</template>

<script>
import Vue from "vue";
import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  props: {
    cname: {
      type: String,
      default() {
        return "swiper";
      }
    },
    options: {
      type: Object,
      default() {
        return {
          autoPlay: true,
          loop: true,
          pagination: {
            el: ".swiper-pagination"
          },
          notNextTick: true
        };
      }
    },
    items: {
      type: Array,
      default() {
        //{href:'',src:''}  默认数据格式
        return [];
      }
    }
  },
  data() {
    return {};
  },
  components: {
    swiper,
    swiperSlide
  },
  methods: {},
  mounted() {}
};
</script>

<style lang="scss">
@import "~swiper/dist/css/swiper.css";
.swiper-pagination-bullet {
  width: 8px;
  height: 8px;
  border: 2px solid #fff;
  background: rgba($color: #000000, $alpha: .4);
}
</style>
