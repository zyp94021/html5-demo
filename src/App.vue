<template>
  <div id="app">
    <sidebar></sidebar>
    <div id="content">
      <p>内容</p>
    </div>
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar.vue";

export default {
  components: {Sidebar},
  name: 'app'
}
</script>

<style lang="scss">
  #app{
    #content{
      position: absolute;
      top:0px;
      right: 0px;
      left:350px;
    }
  }
</style>
