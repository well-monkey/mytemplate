<template>
  <div>
    <div class="navbanner">
        <swiper loop auto :list="demo06_list" :index="demo06_index" @on-index-change="demo06_onIndexChange">      
        </swiper>
       <!--  <p>current index: {{demo06_index}}</p> -->
    </div>
  </div>
</template>

<script>
import { Swiper, GroupTitle, SwiperItem, XButton, Divider } from 'vux'
const baseList = [{
  url: 'javascript:',
  img: 'https://static.vux.li/demo/1.jpg',
  title: '送你一朵fua'
}, {
  url: 'javascript:',
  img: 'https://static.vux.li/demo/2.jpg',
  title: '送你一辆车'
}, {
  url: 'javascript:',
  img: 'https://static.vux.li/demo/3.jpg',
  title: '送你一次旅行'
}]
const urlList = baseList.map((item, index) => ({
  url: 'http://m.baidu.com',
  img: item.img,
  title: ``
}))
export default {
  name:'navbanner',
  components: {
    Swiper,
    SwiperItem,
    GroupTitle,
    XButton,
    Divider
  },
  data () {
    return {
      demo06_list: urlList,
      demo06_index: 0,    
      swiperItemIndex: 1
    }
  },
  methods:{
    tohelloPage:function(){
      this.$router.push({path:"/hello"})
    },
    demo06_onIndexChange (index) {
      this.demo06_index = index
    },
  }
}
</script>

<style>
.vux-demo {
  text-align: center;
}
.logo {
  width: 100px;
  height: 100px
}
</style>
