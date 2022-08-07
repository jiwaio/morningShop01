<template>
  <div class="about">
    <div class="container">
<!--  图片展示    -->
      <b-jumbotron>
        <template v-slot:header>更多 &nbsp; consulting service</template>
        <div style="width: 100%; height: 20%"></div>
        <template v-slot:lead>
          联系我们：
        </template>

        <hr class="my-4">
        <div class="flexText">
          <p>电话：</p>
          <p>134-1577-2789</p>
        </div>
        <div class="flexText">
          <p>微信：</p>
          <p>wxid_eh0p1xdkr72s22</p>
        </div>
        <div class="flexText">
          <p>qq邮箱:</p>
          <p>955907628@qq.com</p>
        </div>
      </b-jumbotron>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import Footer from "@/components/Footer";
export default {
  name: 'about',
  data(){
    return {

    }
  },
  components:{
    Footer
  }
}
</script>

<style lang="less" scoped>
.flexText {
  display: flex;
  flex-flow: row nowrap;
  justify-content: left;
  > p:nth-child(1){
    text-align: center;
    width: 150px;
    font-size: 16px;
  }
  > p:nth-child(2){
    color: #545454;
    width: 300px;
    font-size: 15px;
  }
}
.jumbotron{
  background-color: white;
}
.about{
  min-width: 100%;
}
.footer {
  position: fixed;
}

@media (min-width: 575px) {
  .display-3 {
    font-size: 3.5rem;
    font-weight: 300;
    line-height: 2.2;
  }
}
@media (max-width: 575px) {
  .display-3 {
    font-size: 1.8rem;
    font-weight: 400;
    line-height: 3.2;
  }
}
</style>
