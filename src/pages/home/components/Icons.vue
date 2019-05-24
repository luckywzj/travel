<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index" >
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class="icon-img">
            <img
              class="icon-img-content"
              :src="item.imgUrl"
              alt=""
            >
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>

    </swiper>
  </div>
</template>
<script>
export default {
  name: "HomeIcons",
  data() {
    return {
      iconsList: [
        {
          id: "001",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点景点门票景点门票景点门票门票"
        },
        {
          id: "002",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
          desc: "一日游"
        },
        {
          id: "003",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/3ef092d0a89ffddb7f781cda30c8ae49.png",
          desc: "上海上海"
        },
        {
          id: "004",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/f5/c4c9d9830404e602.png",
          desc: "室内娱乐"
        },
        {
          id: "005",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png",
          desc: "动植物园"
        },
        {
          id: "006",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png",
          desc: "世纪公园"
        },
        {
          id: "007",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/cb506456115da181cd1deadfa17bfee9.png",
          desc: "浦建公园"
        },
        {
          id: "008",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png",
          desc: "上海野生"
        },
        {
          id: "009",
          imgUrl:
            "https://img1.qunarzz.com/piao/fusion/1810/50/26ffa31b56646402.png",
          desc: "上海海昌 "
        }
      ]
    };
  },
  computed: {
    pages() {
      const pages = [];
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item)
      })
      return pages
    }
  }
};
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';
.icons>>>.swiper-container {
  height: 0;
  padding-bottom: 50%;
}

.icons {
  overflow: hidden;
  height: 0;
  padding-bottom: 50%;
}

.icon {
  position: relative;
  overflow: hidden;
  float: left;
  width: 25%;
  height: 0;
  padding-bottom: 25%;

  .icon-img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0.44rem;
    box-sizing: border-box;
    padding: 0.1rem;

    .icon-img-content {
      display: block;
      margin: 0 auto;
      height: 100%;
    }
  }
}

.icon-desc {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 0.44rem;
  text-align: center;
  line-height: 0.44rem;
  color: $darkTextColor;
  ellipsis()
}
</style>
