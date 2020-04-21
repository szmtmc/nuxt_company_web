<template>
  <div class="container">
    <header-nav :navindex="2"></header-nav>
    <banner-Bg :list="list"></banner-Bg>
    <Main></Main>
  </div>
</template>

<script>
import HeaderNav from '~/components/HeaderNav'
import BannerBg from '~/components/BannerBg'
import Main from '~/components/about/Main'


export default {
  head () {
    return {
      title: '关于百拓-百拓共享'
    }
  },
  data () {
    return {
      list: [{
        id: 2,
        h2: '关于百拓',
        p: '我们着眼未来，相信前程似锦'
      }]
    }
  },
  layout: 'default',
  components: {
    HeaderNav,
    BannerBg,
    Main
  }
}
</script>

<style>
</style>
