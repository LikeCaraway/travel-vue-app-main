<template>
    <div class="top-box">
        <!-- 导航栏 -->
        <Navbar></Navbar>
        <!-- 搜索框 -->
        <Search></Search>
        <!-- 视频背景 -->
        <div class="background-mv">
            <video autoplay loop muted> 
                <source  src="../assets/maldivesVideo.mp4"/>
            </video>
            <!-- 原视频色彩比较鲜艳，不适合直接作背景，想要的效果像是用一层淡黑色的幕布蒙在上面 -->
            <div class="overlay"></div>
        </div> 

        
    </div>
</template>

<script setup>
import Navbar from './Navbar.vue';
import Search from './Search.vue';
</script>

<style lang="scss" scoped>
.background-mv{
    width: 100%;
    height: 100vh;
    position: relative;
    color: #fff;
    z-index: -1;
    video{
        width: 100%;
        height: 100%;
        //超出部分被剪掉
        object-fit: cover;
    }
}
.overlay{
        background-color: rgba(0,0,0,0.2);
        position: absolute;
        width: 100%;
        height: 100vh;
        top: 0;
        left: 0;
}

</style>