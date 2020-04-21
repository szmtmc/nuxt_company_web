<template>
  <div class="banner-wrap">
    <div class="wrapper">
      <el-carousel :interval="5000" arrow="hover" height="780px">
        <el-carousel-item v-for="item in picArr" :key="item.id">
          <div class="imgwrapepr">
            <div class="banner-info">
              <h1>{{item.h1}}</h1>
            </div>
            <img :src="item.pic_url" />
          </div>
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      picArr: [
        {
          id: 201910111,
          title: "固定1",
          h1: '构建战略级科技服务的生态系统',
          pic_url: "https://img.baitton.com/slide-1.jpg"
        },
        {
          id: 201910112,
          title: "固定2",
          h1: '成功源于共享 创新成就未来',
          pic_url: "https://img.baitton.com/slide-2.jpg"
        },
        {
          id: 201910113,
          title: "固定3",
          h1: '拓知共行 服务至上',
          pic_url: "https://img.baitton.com/slide-3.jpg"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.banner-wrap {
  display: flex;
  justify-content: center;
  width: 100%;
  height: 780px;
  overflow: hidden;
  position: relative;
}
.wrapper {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  z-index: 0;
}
.imgwrapepr {
  height: 884px;
  width: 100%;
  margin: 0 auto;
  position: relative;
}
.bannerimg {
  width: 100%;
  height: 100%;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
.banner-info {
  position: absolute;
  top: 300px;
  left: 50%;
  transform: translateX(-50%);
}
.banner-info h1 {
  color: #fff;
  font-size: 50px;
  font-weight: 300;
  line-height: 50px;
  margin-bottom: 25px;
}
.banner-info p {
  color: #fff;
  font-size: 17px;
  font-weight: 400;
}
.wrapper {
  /deep/ .el-carousel__indicators--horizontal {
    bottom: 0px;
  }
}
img {
  width: 100%;
  height: 100%;
}
@media screen and (max-width: 767px) {
  .banner-info h1 {
    width: 100%;
    word-break: keep-all;
    word-break: normal;
    padding-right: 30px;
  }
  .banner-info {
    width: 60%;
    word-wrap: break-word;
    word-break: normal;
    text-align: center;
    margin-left: 5%;
    padding-right: 5%;
    position: absolute;
    top: 300px;
  }
}
@media screen and (max-width: 496px) {
  .banner-wrap {
    height: 586px;
  }
  .banner-info {
    top: 260px;
  }
  .wrapper {
    /deep/ .el-carousel__indicators--horizontal {
      bottom: 200px;
    }
  }
  .wrapper {
    /deep/ .el-carousel__arrow {
      display: block !important;
    }
  }
  .wrapper {
    /deep/ .banner-info h1 {
      font-size: 30px;
      line-height: 38px;
      word-break: keep-all;
    }
  }
}
</style>