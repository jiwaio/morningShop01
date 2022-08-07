<template>
<div>
<!--  <p>CAPE 系列中最小的成员不仅站立，而且特别优雅。完全由无烟煤粉末涂层钢制成，并且由于锥形材料厚度，边桌看起来特别精致。</p>-->
    <div v-b-toggle="'collapse-2'" class="m-1" @click="showAdd = !showAdd">产品详情
      <span class="spanText" v-show="showAdd">＋</span>
      <span class="spanText" v-show="!showAdd">－</span></div>
    <b-collapse id="collapse-2">
      <b-card>
        <div class="flexText">
          <p>框架：</p>
          <p>说dv和你审批ID说看视频大V技术的 神盾局迫的</p>
        </div>
        <div class="flexText">
          <p>详情：</p>
          <p>说dv和你</p>
        </div>
      </b-card>
    </b-collapse>
  </div>
</template>

<script>
export default {
name: "collapse",
  data(){
    return {
      showAdd:true,
    }
  },

}
</script>

<style scoped lang="less">
.m-1 {
  margin: 1.25rem !important;
  position: relative;
  .spanText {
    margin-left: 150px;
    font-size: 24px;
    color: #545454;
    transition: all 2s;
  }
}
.card-body{
  display: flex;
  flex-flow: column nowrap;
  .flexText {
    display: flex;
    flex-flow: row nowrap;
    justify-content: left;
    > p:nth-child(1){
      width: 120px;
      font-size: 16px;
    }
    > p:nth-child(2){
      color: #545454;
      width: 300px;
      font-size: 15px;
    }
  }
}

</style>