<template>
  <layout>
    <x-nav slot="header" back="/" title="Swiper"></x-nav>
    <x-body slot="body" style="background:#fff" v-if="pageState.into">
      <swiper :active.sync="active" :options="options" class="swiper-demo">
        <swiper-item v-for="(item,index) in images" :key="index">
          <img :src="item" class="swiper-img" />
        </swiper-item>
      </swiper>
    </x-body>
  </layout>
</template>

<script>
import { children } from 'utils/mixins/page'
import {Swiper, SwiperItem} from '../components/swiper' // import {Swiper, SwiperItem} from 'vx-ui/lib/swiper'
export default {
  components: {
    Swiper,
    SwiperItem
  },
  mixins: [children],
  data () {
    return {
      images: [
        'http://assets.bittyos.com/images/swiper/01.jpg',
        'http://assets.bittyos.com/images/swiper/02.jpg',
        'http://assets.bittyos.com/images/swiper/03.jpg',
        'http://assets.bittyos.com/images/swiper/04.jpg',
        'http://assets.bittyos.com/images/swiper/05.jpg'
      ],
      active: 0,
      options: {
        speed: 500
      }
    }
  }
}
</script>

<style lang="scss">
  .swiper-demo{
    img{
      max-width:100%;
    }
    .swiper-img{
      min-height:120px;
    }
  }
</style>
