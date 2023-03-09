<template>
    <div class="selects-img">
        <img :src="props.src" alt="/">
        <div class="overlay">
            <p>{{props.text}}</p>
            <svg t="1678334463199" v-show="!isLikes" @click="likes" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2337" width="200" height="200"><path d="M698.4 212c46.2 0 89.8 18.2 122.5 51.2 68.1 68.6 68.1 180.2 0 248.7L531 804c-6.5 6.6-13.9 8-19 8s-12.4-1.4-19-8L203.1 511.9c-68.1-68.6-68.1-180.2 0-248.7 32.8-33 76.3-51.2 122.5-51.2s89.8 18.2 122.5 51.2l63.9 64.3 63.9-64.3c32.7-33 76.3-51.2 122.5-51.2m0-90c-67.5 0-134.9 25.9-186.4 77.8-51.5-51.9-118.9-77.8-186.4-77.8s-134.9 25.9-186.4 77.8c-102.9 103.7-102.9 271.8 0 375.6l289.9 292.1C452 890.5 482 902 512 902c30 0 60-11.5 82.8-34.6l289.9-292.1c102.9-103.7 102.9-271.8 0-375.6-51.4-51.8-118.8-77.7-186.3-77.7z" fill="#dbdbdb" p-id="2338"></path></svg>
            <svg t="1678334961624" v-show="isLikes" @click="likes" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="4328" width="200" height="200"><path d="M512 901.746939c-13.583673 0-26.122449-4.179592-37.093878-13.061225-8.881633-7.314286-225.697959-175.020408-312.424489-311.379592C133.746939 532.37551 94.040816 471.24898 94.040816 384.522449c0-144.718367 108.146939-262.269388 240.326531-262.269388 67.395918 0 131.657143 30.82449 177.632653 84.636735 45.453061-54.334694 109.191837-84.636735 177.110204-84.636735 132.702041 0 240.326531 117.55102 240.326531 262.269388 0 85.159184-37.093878 143.673469-67.395919 191.216327l-1.044898 1.567346c-86.726531 136.359184-303.542857 304.587755-312.424489 311.379592-10.44898 8.359184-22.987755 13.061224-36.571429 13.061225z" fill="#d81e06" p-id="4329"></path></svg>
        </div>
    </div>
</template>

<script setup>
import {ref} from 'vue';
   const props = defineProps(['src','text']);
   const isLikes = ref(false);

   //点赞的回调函数
   const likes = () => {
        isLikes.value = !isLikes.value;
        if( isLikes.value === true){
            ElNotification({
            message: '点赞成功，谢谢您的关注!',
            type: 'success',
            position:'bottom-right',
            duration:2500
            })
        }
        
   }
</script>

<style lang="scss" scoped>
.selects-img{
    position: relative;
}
.selects-img img{
    height: 100%;
    width: 100%;
    object-fit: cover;
}
.overlay{
    position: absolute;
    top: 0;
    height: 100%;
    width: 100%;
    z-index: 2;
    left: 0;
    background-color: rgba($color: #000000, $alpha: 0.35);
    display: flex;
    justify-content: flex-start;
    align-items: flex-end;
    p{
        font-size: 2rem;
        position: absolute;
        bottom: 1rem;
        left: 1rem;
        color: white;
    }
    .icon{
        width: 35px;
        height: 35px;
        margin: 0px 5px;
        position: absolute;
        bottom: 1rem;
        right: 1rem;
        transition: all .3s;
    }
    .icon:hover{
        transform: scale(1.2);
        cursor: pointer;
    }

}
</style>