<template>
  <div class="icons">

    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">

        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src='item.imgUrl'/>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
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
      iconsList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '景点门票'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '一日游'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '上海必游'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '上海海昌'
        },
        {
          id: '0005',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '打卡圣地'
        },
        {
          id: '0006',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '泡温泉'
        },
        {
          id: '0007',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '上海欢乐谷'
        },
        {
          id: '0008',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '野生动物园'
        },
        {
          id: '0009',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '第九条数据'
        }

      ]

    }
  },
  computed: {

    pages () {
      const pages = []
      this.iconsList.forEach(function (item, index) {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}

</script>

<style scoped lang="stylus">

  @import '~styles/mixins.styl'

  .icons{
    margin-top: .2rem;
    overflow: hidden;
    height:0;
    padding-bottom:50%;

  }

  .icon{
    position: relative;
    overflow: hidden;
    float: left;
    width:25%;
    height:0;
    padding-bottom: 25%;
  }

  .icon-img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom:.44rem;
  }

  .icon-img-content{
    height:100%;
    margin: 0 auto;
    display: block;
  }

  .icon-desc{
    position: absolute;
    left: 0;
    right: 0;
    bottom:.10rem;
    line-height: .44rem;
    color: #333;
    ellipsis()
  }

  .swiper-container{
    height:0;
    padding-bottom:50%;
  }
</style>
