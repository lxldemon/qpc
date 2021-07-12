<template>
    <div id="QuestionListComponent">
        <div class="category">
            <el-button-group v-for="(item,i) in categorys" :key="i">
                <el-button type="primary" size="mini" :icon="item.icon"></el-button>
                <el-button type="primary" size="mini">{{item.name}}</el-button>
                &nbsp;&nbsp;&nbsp;
            </el-button-group>
        </div>
        <div class="questionList">
            <el-tabs type="border-card">
                <el-tab-pane>
                    <span slot="label"><i class="el-icon-date"></i> 我的行程</span>
                    我的行程
                </el-tab-pane>
                <el-tab-pane label="消息中心">消息中心</el-tab-pane>
                <el-tab-pane label="角色管理">角色管理</el-tab-pane>
                <el-tab-pane label="定时任务补偿">定时任务补偿</el-tab-pane>
            </el-tabs>
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
    .questionList{
        clear: both;
        float: left;
        margin-top: 19px;
    }
</style>
