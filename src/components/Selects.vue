<template>
    <div class="container">
        <div class="selects-box">
            <SelectsImg :src="BoraBora" class="selectsImg" text="Bora Bora"></SelectsImg>
            <SelectsImg :src="BoraBora2" class="selectsImg" text="Emerald Bay"></SelectsImg>
            <SelectsImg :src="Maldives" class="selectsImg" text="Maldives"></SelectsImg>
            <SelectsImg :src="Maldives2" class="selectsImg" text="Grenada"></SelectsImg>
            <SelectsImg :src="Maldives3" class="selectsImg" text="Barbados"></SelectsImg>
            <SelectsImg :src="KeyWest" class="selectsImg" text="Key West"></SelectsImg>
        </div>
        
    </div>
</template>

<script setup>
import BoraBora from '../assets/borabora.jpg';
import BoraBora2 from '../assets/borabora2.jpg';
import Maldives from '../assets/maldives.jpg';
import Maldives2 from '../assets/maldives2.jpg';
import Maldives3 from '../assets/maldives3.jpg';
import KeyWest from '../assets/keywest.jpg';

import SelectsImg from './SelectsImg.vue';

</script>

<style lang="scss" scoped>
.selects-box{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 2rem 0;
    .selectsImg{
        width: 31%;
        margin: .3rem;
    }
}
@media screen and (max-width: 760px) {
    .selects-box{
        flex-direction: column !important;
        .selectsImg{
            width: 100% !important;
        }
    }
    
}
</style>