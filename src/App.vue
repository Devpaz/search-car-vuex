<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <vuex-search-list></vuex-search-list>
    <vuex-search-form></vuex-search-form>
  </div>
</template>

<script>
import VuexSearchList from './components/VuexSearchList.vue'
import VuexSearchForm from './components/VuexSearchForm.vue'

export default {
  name: 'App',
  components: {
    VuexSearchList,
    VuexSearchForm
  }
}
</script>
