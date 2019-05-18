<template>
  <div>
    <!-- 搜索条 -->
    <div class="search">
      <div class="search-bar">
        <icon type='search'/>
        <span>搜索</span>
      </div>
    </div> 
    <!-- 轮播图 -->
    <swiper :indicator-dots='indicatorFlag'>
      <swiper-item :key='index' v-for="(item, index) in imgUrls">
        <image :src="item" class="slide-image"/>
      </swiper-item>
    </swiper>

  </div>
</template>
<script>
export default {
  data () {
    return {
      imgUrls: [
        'https://images.unsplash.com/photo-1551334787-21e6bd3ab135?w=640',
        'https://images.unsplash.com/photo-1551214012-84f95e060dee?w=640',
        'https://images.unsplash.com/photo-1551446591-142875a901a1?w=640'
      ],
      // 控制显示底部圆点
      indicatorFlag: true
    }
  }
}
</script>
<style scoped>
.search {
  background-color: #EB4450;
  padding: 10px;
} 
.search .search-bar {
  text-align: center;
  background-color: #fff;
}
.search .search-bar icon {
  vertical-align: middle;
}
.slide-image {
  width: 750rpx;
}
</style>