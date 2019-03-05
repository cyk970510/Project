<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
  </div>
</template>

<script>
import CityHeader from './components/header.vue'
import CitySearch from './components/Search'
export default {
  name: 'City',
  components: {
    CitySearch: CitySearch,
    CityHeader: CityHeader
  }
}
</script>

<style lang="stylus" scoped>

</style>
