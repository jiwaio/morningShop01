<template>
  <!--  图片展示  -->
  <div class="container" style="margin-top: 3rem">
      <h4>更多展示</h4>
    <b-card-group columns>
    <b-card
        :img-src="picture.imgC"
        img-alt="Image"
        img-top
        v-for="(picture,index) in productPicture"
        :key="index"
    >
<!--      <b-card-text>-->
<!--        This is a wider card with supporting text below as a natural lead-in to additional content.-->
<!--        This content is a little bit longer.-->
<!--      </b-card-text>-->
<!--    </b-card>-->
<!--    </b-card-group>-->
<!--      <b-card-group deck>-->
<!--        <b-card-->
<!--            v-for="(picture,index) in productPicture"-->
<!--            :img-src="picture.imgC"-->
<!--            :key="index">-->
        </b-card>
      </b-card-group>


  </div>
  <!--  图片展示  -->
</template>

<script>
export default {
name: "PictureBottom",
  data(){
    return {
      a:require('@/assets/img/tableLeg/tableLegHome/tableLeg(4).jpg')
    }
  },
  props:{
    productPicture: {
      type: Array
    }
  },
  created() {
    console.log(this.productPicture);
  }
}
</script>

<style scoped lang="less">
.card-body {
  padding: 0;
}
@media (min-width: 576px){
  .card-columns {
    -moz-column-gap: 3rem;
    padding-top: 1rem ;
}
  .card{
    &:hover {
      transform: scale(1.04);
      //top:-5px;
      transition: all 2s;
    }
  }
}
</style>