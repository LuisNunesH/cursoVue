<template>
    <h1>Oii</h1>
</template>

<script>
    export default {
        name: 'LifeCycle',
        data(){
            return {
                nome: 'Maria'
            }
        },
        beforeCreate(){
            console.log('beforeCreate')
        },
        created(){
            this.lifeCycle()
            console.log('created')
        },
        beforeMount(){
            console.log('beforeMount')
        },
        mounted(){
            this.lifeCycle()
            console.log('mounted')
        },
        beforeUpdate(){
            console.log('beforeUpdate')
        },
        updated(){
            console.log('updated')
        },
        beforeDestroy(){
            console.log('beforeDestroy')
        },
        destroyed(){
            console.log('destroyed')
        },
        methods: {
            lifeCycle(){
                console.log('lifeCycle')
            }
        }
    }
</script>