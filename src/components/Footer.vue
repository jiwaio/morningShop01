<template>
<div class="footer">
  <div class="textR container">© 2022，更多 【 morning 】。版权所有</div>
</div>
</template>

<script>
export default {
name: "Footer"
}
</script>

<style scoped lang="less">
.footer{
  position: relative;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 5rem;
  line-height: 5rem;
  background-color: #cfcfcf;
  margin-top: 2rem;
  .textR{
    font-size: .8rem;
    color: #545454;
  }
}

@media (max-width: 575px) {
  .footer {
    height: 3rem;
    line-height: 3rem;
  }
}
</style>