<template>
  <div class="container">
    <header-nav :navindex="1"></header-nav>
    <banner-Bg :list="list"></banner-Bg>
    <BussinessItem :businessList="businessList"></BussinessItem>
  </div>
</template>

<script>
import HeaderNav from '~/components/HeaderNav'
import BannerBg from '~/components/BannerBg'
import BussinessItem from '~/components/bussiness/BussinessItem'

import axios from 'axios'
import url from '../middleware/api'

export default {
  head () {
    return {
      title: '业务服务-百拓共享'
    }
  },
  data () {
    return {
      list: [{
        id: 1,
        h2: '业务&服务',
        p: '我们从企业业务实际出发，提出富有前瞻性的解决方案，并将策略和执行结合起来。'
      }],
      businessList: []
    }
  },
  mounted () {
    axios.get(url.producDetailtList).then(res => {
      this.businessList = res.data.list
    })
  },
  layout: 'default',
  components: {
    HeaderNav,
    BannerBg,
    BussinessItem
  }
}
</script>

<style>
</style>
