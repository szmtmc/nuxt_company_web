<template>
  <div class="container">
    <header-nav :navindex="0"></header-nav>
    <banner :bannerList="bannerList"></banner>
    <Product :list="list1"></Product>
    <Product :list="list2"></Product>
    <Product :list="list3"></Product>
    <Partner :partnerList="partnerList"></Partner>
    <Expert :expertList="expertList"></Expert>
    <Join></Join>
  </div>
</template>

<script>
import HeaderNav from '~/components/HeaderNav'
import Banner from '~/components/home/Banner'
import Product from '~/components/home/Product'
import Partner from '~/components/home/Partner'
import Expert from '~/components/home/Expert'
import Join from '~/components/home/Join'

import axios from 'axios'
import url from '../middleware/api'
export default {
  head () {
    return {
      title: '首页-百拓共享'
    }
  },
  data () {
    return {
      bannerList: [],
      list1: [],
      list2: [],
      list3: [],
      partnerList: [],
      expertList: []
    }
  },
  mounted () {
    axios.get(url.bannerLists).then(res => {
      this.bannerList = res.data.img
    })
    axios.get(url.productLists).then(res => {
      this.list1 = res.data.list
    })
    axios.get(url.productLists).then(res => {
      this.list2 = res.data.list
    })
    axios.get(url.productLists).then(res => {
      this.list3 = res.data.list
    })
    axios.get(url.partnerList).then(res => {
      this.partnerList = res.data.list
    })
    axios.get(url.expertList).then(res => {
      this.expertList = res.data.list
    })
  },
  layout: 'default',
  components: {
    HeaderNav,
    Banner,
    Product,
    Partner,
    Expert,
    Join
  }
}
</script>

<style>
</style>
