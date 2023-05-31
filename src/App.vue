<template>
    <div class="container">

        <el-card class="card_main" shadow="always">

            <div class="title">今日猫粮盲盒</div>

            <el-text>
                每天领一些网盘资源(猫粮),日积月累就多啦,你喜欢的猫粮还在采集,也许明天就有啦!
                <el-icon>
                    <Bell />
                </el-icon>
            </el-text>
            <br>
            <el-button @click="isdisplay = true" class="star" type="warning" :icon="Star" circle />


        </el-card>


    </div>


    <!-- 弹出层 -->
    <el-dialog class="dialog" v-model="isdisplay" :show-close="false">

        <el-card class="dialog_card" shadow="always">

            <div>真好奇~里面会是什么呢？</div>


            <el-popover :visible="visible" placement="top" :width="380">
                <p>这里的资源链接每天都会更新哦，记得每天都来点一下~</p>
                <template #reference>
                    <el-button @click="accessing_resources()" class="star" type="warning" :icon="Star" circle />
                </template>
            </el-popover>



            
            <el-divider />
            <div>联系我们:killianverenawn8488#gmail.com</div>
            <div>均为公开资源，若不慎涉及版权，请立即联系我们！</div>
        </el-card>



    </el-dialog>
</template>



<script >
export default {

    data() {

        return {

            isdisplay: false,


        }
    },
    methods:{
        accessing_resources(){

            this.isdisplay=false
        }


    }
}


</script>

<style scoped>
.card_main {

    height: 500px;
    width: 1000px;
    padding: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.container {

    display: flex;
    justify-content: center;
    align-items: center;
}

.title {

    font-family: 'cat', sans-serif;
    font-size: 50px;
    margin-bottom: 20px;

}

.star {

    margin-top: 20px;
    height: 50px;
    width: 50px;
}

.dialog_card {

    height: 300px;
    margin-bottom: 30px;
    margin-left: 20px;
    margin-right: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;

}
</style>

<script setup>
import { Bell, ElementPlus, Star } from '@element-plus/icons-vue'
</script>