<template>
  <div class="bounce-in-top">
    <div class="example-3d">
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide
          v-for="movie in userRecommandMoviesByKeyword"
          :key=movie.id
        >
          <random-box-cube-item
            :movie="movie"
          ></random-box-cube-item>
        </swiper-slide>
        
        <!-- <div class="swiper-pagination" slot="pagination"></div> -->
      </swiper>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

import RandomBoxCubeItem from '@/components/randombox/RandomBoxCubeItem'


export default {
  name: 'RandomBox',
  components: {
    Swiper,
    SwiperSlide,
    RandomBoxCubeItem
  },
  data() {
      return {
        swiperOption: {
          effect: 'cube',
          grabCursor: true,
          cubeEffect: {
            shadow: true,
            slideShadows: true,
            shadowOffset: 20,
            shadowScale: 0.94
          },
          pagination: {
            el: '.swiper-pagination'
          }
        }
      }
    },
    computed: {
      ...mapState([
        'userRecommandMoviesByKeyword',
      ])
    },
  }
</script>

<style lang="scss" scoped>
  .example-3d {
    position: relative;
    overflow: hidden;
    height: 360px;
    padding: 15px;
  }
  .swiper {
    width: 300px !important;
    height: 300px;
    position: absolute;
    left: 50%;
    top: 50%;
    margin-left: -150px;
    margin-top: -150px;
    .swiper-slide {
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      font-weight: bold;
      // font-size: $font-size-huge * 2;
      background-color: #bed8f548;
      background-position: center;
      background-size: cover;
      // color: $white;
    }
    // .swiper-pagination {
    //   /deep/ .swiper-pagination-bullet.swiper-pagination-bullet-active {
    //     // background-color: $white;
    //   }
    // }
  }
</style>

<style lang="css" scoped>
  /* ----------------------------------------------
 * Generated by Animista on 2021-11-24 9:16:43
 * Licensed under FreeBSD License.
 * See http://animista.net/license for more info. 
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */

/**
 * ----------------------------------------
 * animation bounce-in-top
 * ----------------------------------------
 */
@-webkit-keyframes bounce-in-top {
  0% {
    -webkit-transform: translateY(-500px);
            transform: translateY(-500px);
    -webkit-animation-timing-function: ease-in;
            animation-timing-function: ease-in;
    opacity: 0;
  }
  38% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
            animation-timing-function: ease-out;
    opacity: 1;
  }
  55% {
    -webkit-transform: translateY(-65px);
            transform: translateY(-65px);
    -webkit-animation-timing-function: ease-in;
            animation-timing-function: ease-in;
  }
  72% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
            animation-timing-function: ease-out;
  }
  81% {
    -webkit-transform: translateY(-28px);
            transform: translateY(-28px);
    -webkit-animation-timing-function: ease-in;
            animation-timing-function: ease-in;
  }
  90% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
            animation-timing-function: ease-out;
  }
  95% {
    -webkit-transform: translateY(-8px);
            transform: translateY(-8px);
    -webkit-animation-timing-function: ease-in;
            animation-timing-function: ease-in;
  }
  100% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
            animation-timing-function: ease-out;
  }
}
@keyframes bounce-in-top {
  0% {
    -webkit-transform: translateY(-500px);
            transform: translateY(-500px);
    -webkit-animation-timing-function: ease-in;
            animation-timing-function: ease-in;
    opacity: 0;
  }
  38% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
            animation-timing-function: ease-out;
    opacity: 1;
  }
  55% {
    -webkit-transform: translateY(-65px);
            transform: translateY(-65px);
    -webkit-animation-timing-function: ease-in;
            animation-timing-function: ease-in;
  }
  72% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
            animation-timing-function: ease-out;
  }
  81% {
    -webkit-transform: translateY(-28px);
            transform: translateY(-28px);
    -webkit-animation-timing-function: ease-in;
            animation-timing-function: ease-in;
  }
  90% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
            animation-timing-function: ease-out;
  }
  95% {
    -webkit-transform: translateY(-8px);
            transform: translateY(-8px);
    -webkit-animation-timing-function: ease-in;
            animation-timing-function: ease-in;
  }
  100% {
    -webkit-transform: translateY(0);
            transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
            animation-timing-function: ease-out;
  }
}


  .bounce-in-top {
    -webkit-animation: bounce-in-top 1.1s both;
            animation: bounce-in-top 1.1s both;
  }


</style>