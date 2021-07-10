<template>
    <div id="QuestionListComponent">
        <div class="category">
            <el-button-group v-for="(item,i) in categorys">
                <el-button type="primary" size="mini" :icon="item.icon"></el-button>
                <el-button type="primary" size="mini">{{item.name}}</el-button>
                &nbsp;&nbsp;&nbsp;
            </el-button-group>
        </div>
    </div>
</template>

<script>
    export default {
        name: "QuestionListComponent",
        data(){
            return{
                categorys:[
                    {
                        name:"全部",
                        icon:"el-icon-s-home"
                    },{
                        name:"其他问题",
                        icon:"el-icon-bangzhu"
                    },{
                        name:"软件相关",
                        icon:"el-icon-medal"
                    },{
                        name:"游戏相关",
                        icon:"el-icon-grape"
                    }
                ]
            }
        },methods:{

        },created() {
        }
    }
</script>

<style scoped>
    #QuestionListComponent{
        margin: 0 auto;
        width: 80%;
        font-size: 18px;
    }
    .category{
        float: left;
    }
</style>