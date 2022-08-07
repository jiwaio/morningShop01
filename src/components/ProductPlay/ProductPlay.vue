<template>
<!-- 商品展示 -->
<div class="ProductPlay">
<div class="container">
  <h4 class="headerTitleMax">桌脚</h4>
    <b-card-group columns>
      <h5 class="headerTitleMin">桌脚</h5>
      <b-card v-for="(item, index) in productM" :key="index" :img-src="item.img" img-alt="Image" img-top>
        <b-card-text @click="searchDetail(item)">
         观看更多图片 →
        </b-card-text>
      </b-card>
    </b-card-group>
</div>
</div>
</template>

<script>
import productM from "@/components/ProductPlay/product";
export default {
name: "ProductPlay",
  data(){
    return {
      productM:productM,
    }
  },
  props:{
    pro:[]
  },
  created() {
  },
  methods:{
    searchDetail(product){
      this.$router.push({name: "productDetail", params: product})
    }
  }
}
</script>

<style scoped lang="less">
.card-body{
  padding: .7rem;
  .card-text{
    font-size: 15px;
    color: #545454;
    &:hover {
      color: cornflowerblue;
    }
  }
}

.card{
  overflow: hidden;
  img:hover{
    transform: scale(1.05);
    transition: 2s all;
  }
}


@media (max-width: 575px) {
    .headerTitleMax {
      display: none;
    }
  .headerTitleMin{
    text-align: left;
    margin-left: 2rem;
  }
    .card-columns {
      margin-left: 20%;
      text-align: center;
    }
  .card-body{
    padding: .4rem;
    .card-text{
      font-size: 14px;
      color: #545454;
    }
  }
  }
@media (min-width: 575px) {
  .headerTitleMin {
    display: none;
  }
  .ProductPlay {
    margin-top: 2rem;
    .card-columns .card {
      width: 100%;
    }
  }
}
</style>