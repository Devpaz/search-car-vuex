<template>
  <div id="app">
    <b-container>
      <h1 class="text-center text-muted mt-2 mb-4">Buscador Vuex</h1>
      <vuex-search-form></vuex-search-form>
      <vuex-search-list></vuex-search-list>
    </b-container>
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
