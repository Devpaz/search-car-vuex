<template>
  <div id="app">
    <vuex-search-form></vuex-search-form>
    <vuex-search-list></vuex-search-list>
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
