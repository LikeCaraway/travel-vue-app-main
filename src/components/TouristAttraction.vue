<template>
    <div class="container">
        <div class="pictrue-show-box">
            <h1>旅游胜地</h1>
            <h4>拍摄于加勒比海</h4>
            <div class="pictrue-box">
                <div class="pictrue-left-box">
                    <img src="../assets/maldives3.jpg" alt="/">
                </div>
                <div class="pictrue-right-box">
                    <img src="../assets/borabora.jpg" alt="/">
                    <img src="../assets/borabora2.jpg" alt="/">
                    <img src="../assets/keywest.jpg" alt="/">
                    <img src="../assets/maldives.jpg" alt="/" />
                </div>
                
            </div>
        </div>
    </div>
</template>

<script setup>
    
</script>

<style lang="scss" scoped>
.pictrue-show-box{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2.5rem 0;
    h4{
        font-weight: normal;
        padding: 1.5rem;
    }

    .pictrue-box{
        width: 100%;
        height: 500px;
        display: flex;
        padding: 10px;
        height: 100%;
        .pictrue-left-box{
            width: 60%;
            margin: 5px;
        }
        .pictrue-left-box img{
            width: 100%;
            transition: all .3s;
        }
        .pictrue-left-box img:hover{
                cursor: pointer;
                transform: scale(1.02);
         }
        .pictrue-right-box{
            display: flex;
            flex-wrap: wrap;
            width: 40%;
            height: 100%;
            img{
                flex-grow:1;
                width: 200px;
                height: 186px;
                object-fit: cover;
                margin: 5px;
                transition: all .3s;
            }
            img:hover{
                cursor: pointer;
                transform: scale(1.1);
            }
            
            
        }
    }
}
@media screen and (max-width: 1280px) and (min-width:760px){
    .pictrue-right-box{
        height: auto !important;
    }
    .pictrue-right-box img{
        width: inherit !important;
        height: 45.5% !important;
        
    }
}
@media screen and (max-width: 759px) {
    .pictrue-box{
        flex-direction: column;
    }
    .pictrue-left-box{
        width: 100% !important;
        margin: 0 auto !important;
    }
    .pictrue-right-box{
        display: flex;
        flex-wrap: wrap;
        width: 100% !important;
        margin: 5px auto !important;
        height: 100%;
    }
    .pictrue-right-box{
        height: auto !important;
    }
    h1{
       font-size:2.5rem ; 
    }
}
</style>