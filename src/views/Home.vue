<template>
  <div>
    <div class="home">
    </div>
    <HomeExpertsComponent></HomeExpertsComponent>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import HomeExpertsComponent from '@/components/HomeExpertsComponent.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,HomeExpertsComponent
  }
}
</script>

<style>
  .home{
    height: 300px;
    margin:-20px;
    background-size: 100% 100%;
    background: #353b65 url(https://shequ.jb51.net/assets/addons/ask/img/banner.jpg) no-repeat scroll center top;
  }
</style>