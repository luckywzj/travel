<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img
          class="swiper-img"
          :src="item.imgUrl"
          alt=""
        >
      </swiper-slide>
      <div
        class="swiper-pagination"
        slot="pagination"
      ></div>

    </swiper>
    test
  </div>
</template>
<script>
export default {
  name: "HomeSwiper",
  data() {
    return {
      swiperOption: {
       pagination: {
            el: '.swiper-pagination'
       },
       loop:true
      },
      swiperList:[
        {
          id:"001",
          imgUrl:"http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/e1e587f554e5a8372be44a4c6b73a5cf.jpg_750x200_5732f03f.jpg"
        },{
          id:"002",
          imgUrl:"http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/9f39c398e63315d7375efd08028f040e.jpg_750x200_4f536dd8.jpg"
        }
      ]
    };
  }
};
</script>
<style lang="stylus" scoped>
.wrapper>>> .swiper-pagination-bullet-active
  background :#fff
.wrapper
  overflow: hidden
  width :100%
  heigth :0
  padding-bottom  :31.25%
  .swiper-img
    width: 100%;

</style>
