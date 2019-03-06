<template>
  <div id="app">
    <!--exclude="Detail"不让detail页面重新加载-->
    <keep-alive>
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
</style>
