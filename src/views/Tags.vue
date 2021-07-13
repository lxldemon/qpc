<template>
    <div class="tags">
        <el-row :gutter="10">
            <el-col :span='6'><div class="grid-content bg-purple">
                <a href="">Zookerper</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple-light">
                <a href="">python的电子书</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple">
                <a href="">视频编辑软件</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple-light">
                <a href="">python</a>
                <p>暂无介绍</p>
            </div></el-col>
        </el-row>
        <br>
        <el-row :gutter="10">
            <el-col :span='6'><div class="grid-content bg-purple">
                <a href="">Zookerper</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple-light">
                <a href="">python的电子书</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple">
                <a href="">视频编辑软件</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple-light">
                <a href="">python</a>
                <p>暂无介绍</p>
            </div></el-col>
        </el-row>
        <br>
        <el-row :gutter="10">
            <el-col :span='6'><div class="grid-content bg-purple">
                <a href="">Zookerper</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple-light">
                <a href="">python的电子书</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple">
                <a href="">视频编辑软件</a>
                <p>暂无介绍</p>
            </div></el-col>
            <el-col :span='6'><div class="grid-content bg-purple-light">
                <a href="">python</a>
                <p>暂无介绍</p>
            </div></el-col>
        </el-row>
        <br>
        <el-pagination
                background="true"
                layout="prev, pager, next"
                :total="1000">
        </el-pagination>
    </div>
</template>

<script>
    export default {
        name: "Tags"
    }
</script>

<style scoped>
    .tags{
        margin: 0 auto;
        width: 80%;
    }
    .item {
        padding: 18px 0;
    }

    .box-card {
        width: 480px;
    }
    .el-col {
        border-radius: 4px;

    }
    .bg-purple-dark {
        background: #99a9bf;
    }
    .bg-purple {
        background: #d3dce6;
    }
    .bg-purple-light {
        background: #e5e9f2;
    }
    .grid-content {
        border-radius: 4px;
        min-height: 36px;
        background: #fff;
        height: 185px;
        text-align: left;
    }
    .el-pagination.is-background .el-pager li:not(.disabled) {
        background-color: #fff;

    }
    .el-pagination.is-background .el-pager li:not(.disabled).active {
        background-color: #2c3e50;
    color: #fff;
    }
</style>