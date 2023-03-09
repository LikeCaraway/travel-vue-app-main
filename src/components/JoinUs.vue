<template>
    <div class="container">
        <div class="JoinUs-box">
            <h1 >
                加入我们
            </h1>
            <div class="content">
                <div class="left">
                <p>　　你可能从诗句中、书本中、影视作品中和朋友口中看过，听说过不少美景，如果不亲身去看看的话，
                    那些美景将永远只是听说，。人生最好的旅行，就是你在一个陌生的地方，发现一种久违的感动。
                     独自旅行，不受羁绊，没有约束。有一天，背上包，趁年轻，带上自己，有多远，走多远。
                </p>
                <p>　　或带父母去他们想去但从未去过的地方，或与爱人踏遍天涯海角，或带“雏鸟”领略大好山河。
                    与亲朋好友一起，在旅行中留下属于彼此珍贵的回忆吧~
                </p>
                </div>
            <div class="right">
                <el-form class="form" :model="form" label-position="top" label-width="120px">
                    <el-form-item label="目的地">
                        <el-input v-model="form.destination" />
                    </el-form-item>
                    <el-form-item label="出发时间">
                        <el-date-picker
                            v-model="form.checkIn"
                            type="date"
                            placeholder="yy/mm/dd"
                            style="width: 100%"
                        />
                    </el-form-item>
                    <el-form-item label="结束时间">
                        <el-date-picker
                            v-model="form.checkOut"
                            type="date"
                            placeholder="yy/mm/dd"
                            style="width: 100%"
                        />
                    </el-form-item>
                    <button>
                        提交
                    </button>
                </el-form>
            </div>
            </div>
            
        </div>
    </div>
</template>

<script setup>
import { reactive } from 'vue'

const form = reactive({
  destination: '',
  checkIn:'',
  checkOut:''
})
</script>

<style lang="scss" scoped>
.JoinUs-box{
    padding: 2.5rem 0;
    display: flex;
    flex-direction: column;
    h1{
        padding: 1.5rem;
    }
    .content{
        display: flex;
        .left{
            width: 60%;
            p{
                font-size: 1.2rem;
                padding: 0.3rem;
                margin: .2rem  5px;
            }
        }
        .right{
            display: flex;
            justify-content: center;
            align-items: center;
            width: 40%;
            .form{
                width: 90%;
                padding: 0 1rem;
                display: flex;
                flex-direction: column;
                ::v-deep .el-input__wrapper {
                    width: 100% !important;
                }
                ::v-deep .el-form-item__label{
                    font-size: 18px !important;
                }
            }
        }
    }
    

}

@media screen and (max-width: 760px){   
    .content{
        flex-direction: column;
    .left{
            width: 100% !important;
    }
    .right{
            width: 100% !important;
            padding: 1rem 0rem !important;

    }

    }
}
</style>