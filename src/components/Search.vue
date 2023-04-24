<template>
    <div class="search-box">
        <h1>欢迎来到travel.</h1>
        <h2>本站提供优质的旅游资源.</h2>
        <form class="form">
            <div>
                <input type="text" placeholder="想去哪儿？"/>
            </div>
            <div class="search-icon-box">
                <svg t="1678114888430" class="search-icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2310" width="200" height="200"><path d="M949.284321 899.56699 760.985748 711.268416c56.878428-68.365041 91.092671-156.254763 91.092671-252.139577 0-217.868029-176.61651-394.484539-394.484539-394.484539s-394.484539 176.61651-394.484539 394.484539 176.61651 394.484539 394.484539 394.484539c96.92961 0 185.693236-34.960233 254.371408-92.957135l188.114378 188.115402c6.794753 6.794753 15.697517 10.190083 24.602328 10.190083 8.902764 0 17.808598-3.397377 24.602328-10.190083C962.870758 935.184185 962.870758 913.155473 949.284321 899.56699zM457.593879 784.028557c-43.891649 0-86.433558-8.580422-126.44483-25.50386-38.679951-16.360619-73.433476-39.796378-103.294574-69.657476-29.861098-29.861098-53.296857-64.6136-69.657476-103.294574-16.923438-40.010249-25.50386-82.552158-25.50386-126.44483s8.580422-86.433558 25.50386-126.44483c16.360619-38.679951 39.796378-73.433476 69.657476-103.294574 29.861098-29.861098 64.6136-53.296857 103.294574-69.657476 40.010249-16.923438 82.552158-25.50386 126.44483-25.50386 43.891649 0 86.433558 8.580422 126.44483 25.50386 38.679951 16.360619 73.433476 39.796378 103.294574 69.657476 29.860075 29.861098 53.296857 64.6136 69.657476 103.294574 16.923438 40.010249 25.50386 82.552158 25.50386 126.44483s-8.580422 86.433558-25.50386 126.44483c-16.360619 38.679951-39.796378 73.433476-69.657476 103.294574-29.861098 29.861098-64.614623 53.296857-103.294574 69.657476C544.027437 775.448134 501.485529 784.028557 457.593879 784.028557z" fill="#2c2c2c" p-id="2311"></path></svg>
            </div>
        </form>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.search-box{
    position: absolute;
    z-index: 2;
    top: 0;
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    color: white;
    .form{
        display: flex;
        background-color: rgba($color: #eee, $alpha: 0.7);
        border-radius: 5px;
        max-width: 700px;
        margin: .5rem auto;
        padding: 1rem;
        .search-icon-box{
            transition: all .3s;
            .search-icon{
            width: 26px;
            height: 26px;
            cursor: pointer;
            }
        }
        .search-icon-box:hover{
            margin-top:-2px;
        }
        
        input[type=text]{
            width:400px;
            background-color: transparent;
            border: 0px;
            font-size: 20px;
            padding: 3px 0px;
            letter-spacing: 1px;
        }
        input[type=text]:focus{
           outline: none;
        }
    }
}
@media screen  and (max-width:760px) and (min-width:400px){
    input[type=text]{
            max-width: 280px;
    }
}
@media screen and (max-width:400px) {
    input[type=text]{
            max-width: 200px;
    }
}
</style>