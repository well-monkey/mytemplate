<template>
  <div>
    <div class="homepage">
        <banner-page></banner-page>
        <nav-banner></nav-banner>
        <goods-list></goods-list>
    </div>
    
  </div>
</template>

<script>
import bannerPage from '../../components/banner/bannerpage.vue'
import navBanner from '../../components/banner/navbanner.vue'
import goodsList from '../../components/goodslist/goodslist.vue'
export default {
  name:'homepage',
  components: {
      bannerPage,
      navBanner,
      goodsList
  },
  data () {
    return {
      // note: changing this line won't causes changes
      // with hot-reload because the reloaded component
      // preserves its current state and we are modifying
      // its initial state.
      msg: 'Hello World!'
    }
  },
  methods:{
    tohelloPage:function(){
      this.$router.push({path:"/hello"})
    }
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
