<template>
  <div>
    <p style="margin: 1rem">老顾客的日常返图，点击 <a href="/about">->关于我们</a> 找到订做家具的联系方式哦 ~</p>
<!--  商品展示  -->
    <ProductPlay></ProductPlay>
    <Footer></Footer>

<!-- 侧边栏   -->
    <div class="sideBar" ref="sideBar">
        <b-nav vertical class="w-25">
          <b-nav-item active>桌脚</b-nav-item>
          <b-nav-item>凳脚</b-nav-item>
          <b-nav-item>洗手间</b-nav-item>
          <b-nav-item>任何想实现的</b-nav-item>
        </b-nav>
      </div>
  </div>

</template>

<script>
import Footer from "@/components/Footer";
import ProductPlay from "@/components/ProductPlay/ProductPlay";
export default {
  data() {
    return {
    }
  },
  mounted(){
    window.addEventListener('scroll', this.handleScroll,true)
  },
  methods: {
    handleScroll () {
      var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;// 兼容
      if(scrollTop > 85){
        this.$refs.sideBar.style.top = -85 + 'px'
      }else {
        this.$refs.sideBar.style.top = 0
      }
    }
  },
  components:{
    ProductPlay,
    Footer
  }
}
</script>
<style lang="less">

.hello{
  width: 100%;
  height: 50%;
}

@media (min-width: 575px) {
  .carousel{
    height: 50%;
  }
  .sideBar{
    display: none;
  }
}

@media (max-width: 575px) {
  .sideBar {
    position: fixed;
    left: 0;
    top: 0;
    margin-top: 9rem;
    width: 20%;
    height: 30rem;
    .nav-link {
      padding: 1rem 1rem;
    }
    .nav-item{
      box-sizing: content-box;
    }
    ul li {
      border-bottom: #cfcfcf solid 1px;
      &:nth-child(1){
        border-top: #cfcfcf solid 1px;
      }
    }
    a{
      text-align: center;
      width: 5rem;
      display: inline-block;
      font-size: .9rem;
      color: black;
    }
  }
}
</style>
