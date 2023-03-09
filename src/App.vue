<template>
  <Top></Top>
  <Mid></Mid>
  <Footer></Footer>
  <el-tooltip
        class="box-item"
        effect="dark"
        content="回到顶部"
        placement="top"
        show-after="500"
        auto-close="1000"
    >
    <el-backtop :right="40" :bottom="40" class="backtop">
        <template #default="scoped">
          <svg t="1678350887711" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2332" width="200" height="200"><path d="M966.4 668.8l-435.2-432c-9.6-9.6-25.6-9.6-35.2 0l-441.6 432c-9.6 9.6-9.6 25.6 0 35.2 9.6 9.6 25.6 9.6 35.2 0l425.6-416 416 416c9.6 9.6 25.6 9.6 35.2 0S976 678.4 966.4 668.8z" p-id="2333" fill="#1afa29"></path></svg>
        </template>
    </el-backtop>
  </el-tooltip>
</template>

<script setup>
import Mid from './components/Mid.vue';
import Top from './components/Top.vue';
import Footer from './components/Footer.vue';

  
</script>

<style lang="scss" scoped>
.icon{
        width: 35px;
        height: 35px;
        margin: 0px 10px;
        transition: all .3s;
    }
.icon:hover{
    transform: scale(1.1);
    cursor: pointer;
}
@media screen and (max-width: 760px){
  .backtop{
    display: none;
  }
}
</style>