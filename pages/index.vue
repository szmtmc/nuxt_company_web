<template>
  <div class="container">
    <header-nav :navindex="0"></header-nav>
    <banner></banner>
    <Product :list="list1"></Product>
    <Product :list="list2"></Product>
    <Product :list="list3"></Product>
    <Partner></Partner>
    <Expert></Expert>
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


export default {
  head () {
    return {
      title: '首页-百拓共享'
    }
  },
  data () {
    return {
      list1: [{
        id: 1,
        h2_1: '科技信息资源服务',
        p_1: '集成科技政策、科技查新、专利检索、科技培训、专家智库',
        img_1: 'https://img.baitton.com/index-service-1.png'
      }, {
        id: 2,
        h2_1: '知识产权服务',
        p_1: '知识产权战略咨询、知识产权申请与管理、知识产权运营',
        img_1: 'https://img.baitton.com/index-service-2.png'
      }, {
        id: 3,
        h2_1: '科技咨询服务',
        p_1: '科技战略研究咨询、科技项目申报辅导、科技项目管理服务',
        img_1: 'https://img.baitton.com/index-service-3.png'
      }],
      list2: [{
        id: 1,
        h2_1: '科技项目管理',
        p_1: '科技项目评审、可行性评估、项目监理、绩效评价',
        img_1: 'https://img.baitton.com/index-service-4.png'
      }, {
        id: 2,
        h2_1: '创新成果服务',
        p_1: '科技成果评价、科技成果登记、技术交易中介',
        img_1: 'https://img.baitton.com/index-service-5.png'
      }, {
        id: 3,
        h2_1: '创业孵化服务',
        p_1: '孵化器园区运营、孵化天使基金投资、创业企业管理外包',
        img_1: 'https://img.baitton.com/index-service-6.png'
      }],
      list3: [{
        id: 1,
        h2_1: '科技金融服务',
        p_1: '投资顾问、科技保险、企业融资服务',
        img_1: 'https://img.baitton.com/index-service-7.png'
      }, {
        id: 2,
        h2_1: '职业教育培训',
        p_1: '高职教育优化服务、企业人力资源顾问服务、企业内训',
        img_1: 'https://img.baitton.com/index-service-8.png'
      }, {
        id: 3,
        h2_1: '财税顾问服务',
        p_1: '新四板上市服务、尽职调查、报表审计、代理记账服务',
        img_1: 'https://img.baitton.com/index-service-9.png'
      }]
    }
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
