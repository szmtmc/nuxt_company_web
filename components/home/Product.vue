<template>
  <div class="container">
    <div class="card-deck services">
      <div class="card border-0 rounded-0" v-for="item in list" :key="item.id">
        <img class="w-100" :src="item.url" width="461" height="254" />
        <div class="card-body text-center py-5">
          <h5 class="card-title font-weight-bold">{{item.h2}}</h5>
          <p class="card-text">{{item.p}}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Product',
  props: {
    list: Array
  }
}
</script>
<style scoped>
.container {
  max-width: 1450px;
  margin: 0 auto;
  margin-top: 50px;
}
@media screen and (min-width: 576px) {
  .card-deck {
    display: -ms-flexbox;
    display: flex;
    -ms-flex-flow: row wrap;
    flex-flow: row wrap;
    margin-right: -15px;
    margin-left: -15px;
  }
  .card-deck .card {
    -ms-flex: 1 0 0%;
    flex: 1 0 0%;
    margin-right: 15px;
    margin-bottom: 0;
    margin-left: 15px;
  }
}
/* @media screen and (max-width: 576px) {
} */
.card {
  position: relative;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-direction: column;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
  background-color: #fff;
  background-clip: border-box;
  border: 1px solid rgba(0, 0, 0, 0.125);
  border-radius: 5px;
  margin: 0 20px;
  margin-bottom: 20px;
}
.w-100 {
  /* width: 100% !important; */
  transition: all 0.6s;
}
.w-100:hover {
  transform: scale(1.02);
}

img {
  vertical-align: middle;
  border-style: none;
  height: 300px;
}
.text-center {
  text-align: center !important;
}
.font-weight-bold {
  font-weight: 700 !important;
}
.card-title {
  font-size: 22px;
  margin-top: 30px;
  margin-bottom: 10px;
}
.card-text:last-child {
  margin-bottom: 0;
}
.card-text {
  padding-bottom: 30px;
}
</style>
