<template>
    <div>

    </div>
</template>
<script>
    import Datepicker from 'vuejs-datepicker'
    import * as langs from 'vuejs-datepicker/src/locale'
    export default {
        components: {
            Datepicker
        },
        data () {
            return {
                options:[
                    { text: 'Sí', value: true},
                    { text: 'No', value: false},
                ],
                languages: langs,
                lang:'es'
            }
        },
        computed: {
            query: {
                get () {
                return this.$store.state.filter.query
                },
                set (value) {
                this.$store.commit('setFilter', {
                    filter: 'query',
                    value
                })
                }
            },
            from: {
                get () {
                    return new Date(this.$store.state.filter.from, 1, 1)
                },
                set (value) {
                this.$store.commit('setFilter', {
                    filter: 'from',
                    value: new Date(value).getFullYear()
                })
                }
            },
            to: {
                get () {
                return new Date(this.$store.state.filter.to, 1, 1)
                },
                set (value) {
                this.$store.commit('setFilter', {
                    filter: 'to',
                    value: new Date(value).getFullYear()
                })
                }
            },
            min_price: {
                get () {
                return this.$store.state.filter.min_price
                },
                set (value) {
                this.$store.commit('setFilter', {
                    filter: 'min_price',
                    value: parseFloat(value)
                })
                }
            },
            max_price: {
                get () {
                return this.$store.state.filter.max_price
                },
                set (value) {
                this.$store.commit('setFilter', {
                    filter: 'max_price',
                    value: parseFloat(value)
                })
                }
            },
            available: {
                get () {
                return this.$store.state.filter.available
                },
                set (value) {
                this.$store.commit('setFilter', {
                    filter: 'available',
                    value
                })
                }
            },
        },

    }
</script>
