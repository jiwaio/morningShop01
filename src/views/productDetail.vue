<template>
<div>
<!-- 首页图片 -->
  <div class="header-card">
    <b-card
        overlay
        :img-src="product.img"
        img-alt="Card Image"
        text-variant="white"
        title="办公桌"
        sub-title="Subtitle"
    >
<!--   右边产品解析   -->
        <Collapse class="textR"></Collapse>
<!--   右边产品解析   -->
      <b-card-text>
        Some quick example text to build on the card and make up the bulk of the card's content.
      </b-card-text>
    </b-card>

    <!--   右边产品解析   -->
    <Collapse class="textR-min" ></Collapse>
    <!--   右边产品解析   -->

    <!-- 底部图片展示 -->
    <PictureBottom :productPicture="product.children"></PictureBottom>
    <!-- 底部图片展示 -->

  </div>
  <Footer></Footer>
</div>
</template>

<script>
import Footer from "@/components/Footer";
import PictureBottom from "@/components/productDetail/PictureBottom";
import Collapse from "@/components/productDetail/Collapse";
export default {
name: "productDetail",
  data(){
    return {
      product:[],
      a:require('@/assets/img/tableLeg/tableLegHome/tableLeg(4).jpg')
    }
  },
  created() {
    this.product = this.$route.params
  },
  components:{
    Collapse,    //折叠面板
    PictureBottom,  //底部图片展示
    Footer,  //底部
  }
}
</script>

<style scoped lang="less">
.card-title{
  color: black;
}
.card-text{
  color: black;
}

//大于 1400px时
@media (min-width: 1400px) {
  .textR-min{
    display: none;
  }
  .card-body{
    .textR{
      position: absolute;
      width: 20rem;
      height: 20rem;
      color: black;
      //background-color: black;
      top: 2rem;
      right: 5rem;
    }
  }
}

//小于 1400px
@media (max-width: 1400px) {
    .textR {
      display: none;
    }
    .textR-min{
      width: 20rem;
      height: 10rem;
      //background-color: black;
      z-index: 1000;
      margin: 0 auto;
    }
}
@media (min-width: 575px) {
  .card{
    margin: 1vw 10vw;
  }
  .card-img{
    max-width: 50vw;
    height: auto;
  }
}
</style>