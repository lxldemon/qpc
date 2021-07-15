<template>
    <div id="headBox">
        <el-menu
                :default-active="this.$route.path"
                class="el-menu-demo"
                mode="horizontal"
                @select="handleSelect"
                background-color="#222"
                text-color="#fff"
                active-text-color="#ffd04b">
            <el-menu-item index="/" @click="reloadRouter('/')"><img width="25%" src="https://shequimg.jb51.net/assets/addons/ask/img/logo.png" /> 首页</el-menu-item>
            <el-menu-item index="/questions" @click="reloadRouter('/questions')">问答</el-menu-item>
            <el-menu-item index="/articles" @click="reloadRouter('/articles')">文章</el-menu-item>
            <el-menu-item index="/tags" @click="reloadRouter('/tags')">话题</el-menu-item>
            <el-menu-item index="/experts" @click="reloadRouter('/experts')">专家</el-menu-item>
            <el-submenu index="3">
                <template slot="title">个人中心</template>
                <el-menu-item index="2-1">我的主页</el-menu-item>
                <el-menu-item index="2-2">我的提问</el-menu-item>
                <el-menu-item index="2-3">我的文章</el-menu-item>
                <el-menu-item index="2-4">退出</el-menu-item>
            </el-submenu>
        </el-menu>
    </div>

</template>

<script>
    export default {
        name: "Header",
        data() {
            return {
                activeIndex: '1',
                activeIndex2: '1'
            };
        },
        methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            }, reloadRouter(path) {
                this.$router.push(path);
            }
        }
    }
</script>

<style scoped>
.el-menu{
    width: 100%;
}
.el-menu--horizontal>.el-submenu{
    float: right;
}
#headBox{
        width: 80%;
        margin: 0 auto;
    }
</style>
