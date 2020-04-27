<template>
  <div class="container">
    <header-nav :navindex="3"></header-nav>
    <banner-Bg :list="list"></banner-Bg>
    <JoinItem :joinList="joinList"></JoinItem>
    <Join></Join>
  </div>
</template>

<script>
import HeaderNav from '~/components/HeaderNav'
import BannerBg from '~/components/BannerBg'
import JoinItem from '~/components/join/JoinItem'
import Join from '~/components/home/Join'
import axios from 'axios'
import url from '../middleware/api'

export default {
  head () {
    return {
      title: '加入我们-公司名称'
    }
  },
  data () {
    return {
      list: [{
        id: 3,
        h2: '加入我们',
        p: '互联网已成为这个时代的基础设施，利用不断演进的技术，让我们一起构建光辉灿烂的未来。'
      }],
      joinList: []

    }
  },
  mounted () {
    axios.get(url.contactList).then(res => {
      this.joinList = res.data.list
    })
  },
  layout: 'default',
  components: {
    HeaderNav,
    BannerBg,
    JoinItem,
    Join
  }
}
</script>

<style>
</style>
