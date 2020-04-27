<template>
  <div class="container">
    <header-nav :navindex="4"></header-nav>
    <banner-Bg :list="list"></banner-Bg>
    <ContactItem></ContactItem>
  </div>
</template>

<script>
import HeaderNav from '~/components/HeaderNav'
import BannerBg from '~/components/BannerBg'
import ContactItem from '~/components/contact/ContactItem'

export default {
  head () {
    return {
      title: '联系我们-公司名称'
    }
  },
  data () {
    return {
      list: [{
        id: 4,
        h2: '联系我们',
        p: '我们珍惜您每一次的联系，冀望将来光辉的前景。'
      }]
    }
  },
  layout: 'default',
  components: {
    HeaderNav,
    BannerBg,
    ContactItem
  }
}
</script>

<style>
</style>
