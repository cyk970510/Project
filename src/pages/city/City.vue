<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list></city-list>
    <city-alphabet></city-alphabet>
  </div>
</template>

<script>
import CityHeader from './components/header.vue'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
export default {
  name: 'City',
  components: {
    CityAlphabet: CityAlphabet,
    CityList: CityList,
    CitySearch: CitySearch,
    CityHeader: CityHeader
  }
}
</script>

<style lang="stylus" scoped>

</style>
