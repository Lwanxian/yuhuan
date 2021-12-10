<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
/* 全局滚动条样式设置为0 */
::-webkit-scrollbar{
  width: 0px;
}

</style>
