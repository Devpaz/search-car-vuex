<template>
    <div>
        
    </div>
</template>

<script>
    import {mapGetters} from 'vuex'
    export default {
      data () {
        return {
          numberOfColumns: 3
        }
      },
      computed: {
        ...mapGetters(['filteredCars'])
      },
      methods: {
        available (bool) {
          return bool ? 'Sí' : 'No'
        } ,
        carModel (carModel) {
          return `Modelo: ${carModel}`
        },
        blockRandom () {
          return `block-${Math.floor(Math.random() * 6) + 1}`
        }
      }
    }
</script>


<style lang="stylus">
    @import "../assets/search.styl"
</style>