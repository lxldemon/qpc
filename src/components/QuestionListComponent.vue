<template>
    <div id="QuestionListComponent">
        <div class="category">
            <el-button-group v-for="(item,i) in categorys">
                <el-button type="primary" size="mini" :icon="item.icon"></el-button>
                <el-button type="primary" size="mini">{{item.name}}</el-button>
                &nbsp;&nbsp;&nbsp;
            </el-button-group>
        </div>
        <div class="questionList">

            <el-card class="box-card">
                <div slot="header" class="clearfix">
                    <span>卡片名称</span>
                    <span>卡片名称</span>
                    <span>卡片名称</span>
                    <el-button style="float: right; padding: 3px 0" type="text">操作按钮</el-button>
                </div>
                <div v-for="o in 4" :key="o" class="text item">
                    {{'列表内容 ' + o }}
                </div>
            </el-card>


            <el-tabs type="border-card" >
                <el-tab-pane label="最新">

                    <div>
                        <div class="answer">
                            <p>0</p>回答
                        </div>
                        <div class="preview"></div>
                    </div>

                </el-tab-pane>
                <el-tab-pane label="热门">热门</el-tab-pane>
                <el-tab-pane label="悬赏">悬赏</el-tab-pane>
                <el-tab-pane label="未解决">未解决</el-tab-pane>
                <el-tab-pane label="未回答">未回答</el-tab-pane>
                <el-tab-pane label="已解决">已解决</el-tab-pane>
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
        width: 100%;
    }
    .questionList .answer{
        float: left;
    }
</style>
