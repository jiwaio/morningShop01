<template>
  <div>
    <div :style="{height: headerT}"></div>
    <div class="top-fixed" ref="headerTop">
    <b-navbar toggleable="sm" type="light" variant="light" >
      <b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>
      <div class="container">
      <b-navbar-brand>[ Morning ]</b-navbar-brand>
      <b-collapse id="nav-text-collapse" is-nav>
        <b-navbar-nav>
          <router-link :to="item.path" tag="b-nav-text" v-for="item in navPath" :key="item.path" :class="item.path === pathNow ?  'aa' :''">{{ item.text }}</router-link>
        </b-navbar-nav>
      </b-collapse>
      </div>
    </b-navbar>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data(){
    return {
      navPath:[
        {
          text:"首页",
          path:"/"
        },
        {
          text: "关于我们",
          path: "/about"
        }
      ],
      pathNow:'/',
      headerT:0
    }
  },
  watch:{
    $route:{
      handler:function (newval){
        this.pathNow = newval.path
      }
    },
    headerT:{
      handler:function (newval){
        this.pathNow = newval.path
      }
    }
  },
  mounted() {
    this.headerT = this.$refs.headerTop.offsetHeight + 'px'
  }
}
</script>

<style scoped lang="less">
//占位
.place{
  width: 100%;
  height: 80px;
}
.top-fixed{
  z-index: 1000;
  width: 100%;
  position: fixed;
  top:0;
  left: 0;
}
.navbar-text{
  padding: 0 10px;
}
.navbar-collapse{
  float: right;
}
.navbar {
  align-items: baseline;
  justify-content: space-between;
  align-content: flex-start;
  flex-wrap: nowrap;
  flex-direction: row-reverse;
}
.navbar-light .navbar-text{
  &:hover{
    color: black;
   }
}

.aa{
  color: #000000 !important;
  //border-bottom: 2px solid #000000;
}

@media (max-width: 575px) {
  .navbar-text{
    height: 30px;
  }
}
@media (min-width: 575px) {
  .navbar-brand {
    font-size: 1.7rem;
  }
  .navbar-collapse {
    flex-grow: 0;
  }
}
</style>